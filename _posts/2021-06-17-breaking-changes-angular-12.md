---
layout: post
title:  "Some breaking changes in Angular 12"
date:   2021-06-17 18:26:45 +0300
categories: spa angular
image: "/assets/images/Angular-12-Now-Released.png"
author: "Mahefa Abel"
---

![WSO2 APIM](/assets/images/Angular-12-Now-Released.png)

### Breaking changes in Angular 12

#### Animation:

In Angular version 12 features the DOM components that are presently accurately eliminated when the root view is taken out. If you are utilizing SSR and utilize the application's HTML for delivery, you will be required to guarantee that you save the HTML to a variable prior to destroying the application.  
It is additionally conceivable that tests could be unintentionally depending on the old conduct by attempting to discover a component that was not taken out in a past test. However, if that is the situation the failing tests ought to be updated to guarantee they have proper setup code which instates components they depend on.

#### Common:

Methods of the PlatformLocation class, specifically onPopState as well as onHashChange,used to return void. Presently those techniques return works that can be called to eliminate event handlers.  

One of the main Angular 12 improvements is that the strategies for the HttpParams class currently acknowledged string | number | boolean rather than string for the value of a parameter. If you expanded this class in your application, you'll need to update the signatures of your strategies to mirror these changes.  

#### Core:

Angular no longer helps in maintaining Node v10. Previously the ng.getDirectives work tossed an error when in case a given DOM node had no Angular setting related to it. This conduct was conflicting with other troubleshooting utilities under ng namespace, which took care of the present circumstance without raising an exemption. As a major change in Angular 12, the ng.getDirectives work for such DOM nodes would bring about an empty array back from that function.

The type of the APP_INITIALIZER token has been changed to more precisely mirror the types of return values that are taken care of by Angular. Before this, each initializer callback was composed to return any, this is currently Promise <unknown> | Observable <unknown> | void.

In the unlikely event that your application utilizes the Injector.get or TestBed.inject API to infuse the APP_INITIALIZER token, you may have to refresh the code to represent the stricter type.

#### Compiler - CLI:

One of the most interesting  [features of Angular 10](https://www.angularminds.com/blog/article/top-features-of-new-angular-v10.html) was the use of the new IVY extractor to run ng x i18n in one of your applications. One of the new features of Angular 12 is that it no longer generates legacy i18n message-ids through linked libraries. For downstream applications providing translations for these messages, the localize-migrate command-line tool will help migrate their message ids.

#### Form:

Previously ‘min’ and ‘max’ attributes characterized on the <input type=" number"> were disregarded by the Forms module. Currently, the presence of these characteristics would trigger min/max validation logic (if formControl, formControlName or on the other hand ngModel orders are additionally present on a given input) and comparing form control status would mirror that.  

#### Platform browser:

XhrFactory has been moved from @angular/normal/http to @angular/normal.  

```
/// Beforeimport {XhrFactory} from '@angular/common/http';/// Afterimport {XhrFactory} from '@angular/common';
```

**Router**:  
Strict invalid checks will give an account of part conceivably being invalid. The type of the RouterLinkActive.routerLinkActiveOptions input was extended to permit all the more adjusted control. Code that recently read this property may be updated to represent the new type.
