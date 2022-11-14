<template>
    <div>Form validation file</div>

    <form novalidate>
        <div class="row">
            <div class="col-md-6">
                <div><strong>Shipping Information </strong></div>

                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" class="form-control" placeholder="Your Name" />
                </div>

                <div class="form-group">
                    <label for="companyName">Company Name</label>
                    <input type="text" id="companyName" class="form-control" placeholder="Your Company Name" />
                </div>
                <div class="form-group">
                    <label for="address">Address</label>
                    <input type="text" id="address" class="form-control" placeholder="Your address" />
                </div>
                <div class="form-group">
                    <label for="landmark">Landmark</label>
                    <input type="text" id="landmark" class="form-control" placeholder="Your address landmark" />
                </div>
                <div class="row">
                    <div class="form-group col-md-6">
                        <label for="city">City</label>
                        <input id="city" type="text" class="form-control" placeholder="Your City Name" />
                    </div>
                    <div class="form-group col-md-3">
                        <label for="state">State</label>
                        <select id="state" class="form-control">
                            <option>GA</option>
                            <option>CL</option>
                            <option>FL</option>
                            <option>AL</option>
                        </select>
                    </div>
                    <div class="form-group col-md-3">
                        <label for="postalcode">Zipcode</label>
                        <input id="postalcode" type="text" class="form-control" placeholder="Your ZIP Code" />
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div><strong>Billing Information </strong></div>
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" class="form-control" placeholder="Your Name" />
                </div>

                <div class="form-group">
                    <label for="companyName">Company Name</label>
                    <input type="text" id="companyName" class="form-control" placeholder="Your Company Name" />
                </div>
                <div class="form-group">
                    <label for="address">Address</label>
                    <input type="text" id="address" class="form-control" placeholder="Your address" />
                </div>
                <div class="form-group">
                    <label for="landmark">Landmark</label>
                    <input type="text" id="landmark" class="form-control" placeholder="Your address landmark" />
                </div>
            </div>
        </div>
    </form>
</template>


<script>
export default {
    name: "FormValidation",
};
</script>

<style>

</style>