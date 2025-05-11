# General_MVC_Questions

1) What is antiforgery token how it works

   An anti-forgery token (also known as a CSRF token) is a security measure used in web applications to protect against Cross-Site Request Forgery (CSRF) attacks.
  
It generates a unique, secret token for each session or form.

This token is:
------------------
Embedded in the form (hidden field).
Stored on the server (in session or cookie).

When a form is submitted, the server:
--------------------------------
Checks that the token from the request matches the one it issued.
If they don't match, the request is rejected.
@Html.AntiForgeryToken()
[HttpPost]
[ValidateAntiForgeryToken]
public ActionResult SubmitForm(MyModel model) {
    // Process form if token is valid
}

2) What is view state in webforms
 In ASP.NET Web Forms, ViewState is a hidden field that automatically stores the state of controls (like textboxes, dropdowns) between HTTP requests. It makes Web Forms more stateful.
<input type="hidden" name="__VIEWSTATE" value="..." />

3)Model binding 
Model binding in Web Forms allows you to bind data from HTTP requests (like form inputs, query strings, etc.) to method parameters or data-bound controls (like GridView, ListView, etc.) without writing much boilerplate code.
