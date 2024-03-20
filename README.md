# Product Management

![image](https://github.com/stefanoturcarelli/authentication-entity-framework-product-management/assets/67341828/c0ab4b5e-0b63-4fa5-b2d6-f295a466e9c8)

![image](https://github.com/stefanoturcarelli/authentication-entity-framework-product-management/assets/67341828/5a3dfa31-0bab-48b8-baf4-494470244f71)

![image](https://github.com/stefanoturcarelli/authentication-entity-framework-product-management/assets/67341828/34d4eed9-de30-4b13-b5ac-1977fa30ac71)

![image](https://github.com/stefanoturcarelli/authentication-entity-framework-product-management/assets/67341828/f85b0c68-6281-4c6a-8ecb-fb43dfa8f1cf)


## Hide Home nav-link

```html
<div class="menu-titles-container collapse navbar-collapse">
    <ul class="ul-navigation-bar navbar-nav">
        @if (!ViewContext.RouteData.Values["Controller"].ToString().Equals("Home") || !ViewContext.RouteData.Values["Action"].ToString().Equals("Index"))
        {
            <li>@Html.ActionLink("Home", "Index", "Home", new { area = "" }, new { @class = "nav-link" })</li>
        }
        <li>@Html.ActionLink("About", "About", "Home", new { area = "" }, new { @class = "nav-link" })</li>
        <li>@Html.ActionLink("Contact", "Contact", "Home", new { area = "" }, new { @class = "nav-link" })</li>
        <li>@Html.ActionLink("Products", "Index", "Product", new { area = "" }, new { @class = "nav-link" })</li>
    </ul>
    @Html.Partial("_LoginPartial")
</div>
```
