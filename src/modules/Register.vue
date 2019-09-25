<template>
    <center>
        <div id="divFrom" class="col-sm-3 my-sm-5 border rounded" style="margin-left:0.5%">
            <form class="container">
                <center>
                    <h1>Register</h1>
                </center>
                <hr>
                <div>
                    <div class="row">
                        <label for="inputfname">Firstname:</label>
                        <input type="text" class="form-control" id="inputfname" placeholder="Firstname">
                    </div><br>
                    <div  class="row">
                        <label for="inputlname">Lastname:</label>
                        <input type="text" class="form-control" id="inputlname" placeholder="Lastname">
                    </div><br>
                    <div class="row"><br>
                        <label for="inputEmail4">Email:</label>
                        <input type="email" class="form-control" id="inputEmail4" placeholder="Email">
                    </div><br>
                    <div class="row">
                        <label for="inputPassword4">Password:</label>
                        <input type="password" class="form-control" id="inputPassword4" placeholder="Password">
                        <span></span><br><br><br>
                    </div>
                </div>
                <button id="btnSubmit" type="submit" class="btn btn-primary btn-lg btn-block col-sm-5"><h4>Register</h4></button><br>
            </form>
        </div>
    </center>
</template>