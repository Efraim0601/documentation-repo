- All services defined in the content component are safely secured. If you are in a safe environment, want to save more complex contents and get blocked by the security policy you might want to override the security only in the content component.
  title:: security for content management
- Typically when using content/control/WebSiteCms?webSiteId=CmsSite (ie "Edit[ing] WebSite CMS For: CMS Web Site [CmsSite]"), the service updateTextContent may prevent you to save contents with a message like
- #+BEGIN_WARNING
  The Following Errors Occurred: In field [textData] by our input policy, your input has not been accepted for security reason. Please check and modify accordingly, thanks.
  #+END_WARNING
- To override the security you can change definitions of other content services by changing the security on field "textData" from "safe" to "any". That’s of course an example and you may find other similar cases.
- You may also prefer to change the security policy at an upper level. See owasp.properties file.