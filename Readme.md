 $(document).ready(function () {
            // Check for error message and show alert if exists
            var error = @Html.Raw(ViewData["Error"]);
            if (error) {
                ErrorAlert();
            }

            // Check for success message and show alert if exists
            var success = @Html.Raw(ViewData["Success"]);
            if (success) {
                SuccessAlert();
            }
        });

        function ErrorAlert() {
            swal.fire({
                title: "Login Failed",
                text: "Invalid Username or Password!",
                icon: "error"
            });
        }

        function SuccessAlert() {
            swal.fire({
                title: "Registration successful",
                icon: "success"
            });
        }