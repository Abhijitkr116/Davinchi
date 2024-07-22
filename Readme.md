<script src="https://code.jquery.com/jquery-3.7.1.min.js"
        integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo="
        crossorigin="anonymous"></script>
<script src="~/Content/dist/sweetalert2.all.min.js"></script>
<script>
    $(document).ready(function () {
        @Html.Raw(ViewData["Success"]);
    });
        function SuccessAlert() {
            swal.fire({
                title: "Registration successfull",
                icon: "success"
            });
        }
</script>