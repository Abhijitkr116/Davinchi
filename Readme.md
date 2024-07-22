  @if (Session["Username"] != null)
  {
      <a class="nav-link text-light logoutbtn">@Session["Username"]<i class="ri-arrow-down-s-fill"></i></a>


      <ul class="bg-light shadow rounded-2 logout" style="padding: 0;">
          <li class="nav-link d-flex align-items-center"><i class="ri-account-circle-line fs-4"></i><a class="nav-link text-dark">My Profile</a></li>
          <li class="nav-link p-0"><hr class="dropdown-divider" /></li>
          <li class="nav-link d-flex align-items-center"><i class="ri-settings-4-line fs-4"></i><a class="nav-link text-dark">Settings</a></li>
          <li class="nav-link p-0"><hr class="dropdown-divider" /></li>
          <li class="nav-link d-flex align-items-center"><i class="ri-logout-box-r-line fs-4"></i><a href="@Url.Action("Logout", "Restaurant")" class="nav-link text-dark">Logout</a></li>
      </ul>
  }
  else
  {
      @Html.ActionLink("Login", "Login", "Restaurant", new { area = "" }, new { @class = "btn btn-outline-light" })
  }