# Auction-Dashboard
Best Auction Dashboard
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Auction Site</title>

    <style>
        /* .site-menu-div {
            width: 50%;
            float: right;
        }

        .site-menu li {
            float: left;
            padding: 12px 20px;
            background-color: #c493f1;
        }

        .site-menu {
            float: right;
            margin: 42px 0 0;
            list-style: none;
            text-transform: uppercase;
            font-size: 19px;
        }

        .logo {
            float: left;
        }

        a:link {
            color: rgb(17, 15, 15);
        }

        a:hover {
            color: rgb(250, 4, 4);
        }

        a:active {
            color: rgb(165, 11, 185);
        }

        p {
            text-align: center;
            font-size: 60px;
            margin-top: 0px;
        } */

        .navbar {
            display: flex;
            justify-content: space-around;
        }

        .navbar ul {
            display: flex;
            list-style: none;
            justify-content: space-around;
            align-items: center;
            margin: 10% 0;
            background: rebeccapurple;

            padding: 0;
        }

        .navbar ul li a {
            padding: 10px 20px;
            display: block;
            font-size: 20px;
            text-decoration: none;
            color: white;
        }

        .heading {
            text-align: center;
        }

        .images-group {
            display: flex;
            justify-content: space-around;
        }
       .images-group1{
           display:flex;
           flex-direction: column;
       }
        .images-group img {
            width: 20vw;
            object-fit: contain;
            object-position: center;

        }
      
    </style>
</head>

<body>
    <div class="navbar">
        <div class="logo">
            <img src="./Auction.png" width="350px" />

        </div>
        <div class="site-menu-div">
            <ul class="site-menu">

                <li>
                    <a href="./auction1.html" onclick="hide('div1')">Current Bids</a>
                </li>



                <li>
                    <a href="javascrit:void(0)" onclick="hide('div2')">Upcoming Bids</a>

                </li>
                <li>
                    <a href="#completedbids" onclick="hide('div3')">Completed Bids</a>
                </li>

            </ul>
        </div>
    </div>
    <div class="page" id="myDiv" style="display: block">
        <h1 class="heading">Bidding</h1>
        <div class="images-group">

            <div class="images-group1">
                <img src="coffee.jpg" />
                <p style="display:block;"> Habiba
                    250
                    1 jan
                    15 jan</p>
            </div>

            <div class="images-group1">
                    <img src="biryani.jpg" />
                    <p style="display:block;"> biryani</p>
                </div>
               
            <div class="images-group1">
                <img src="mobile.jpg" />
                <p style="display:block;"> biryani</p>
            </div>
           

        </div>
        <div class="images-group">

                <div class="images-group1">
                        <img src="tv.jpg" />
                        <p style="display:block;"> biryani</p>
                    </div>
                   
                    
                       
                        <div class="images-group1">
                                <img src="jacket.jpg" />
                                <p style="display:block;"> biryani</p>
                            </div>

                            <div class="images-group1">
                                    <img src="watch.jpg" />
                                    <p style="display:block;"> biryani</p>
                                </div>
                           
          
           
        </div>

    </div>
    <div id="myDiv2" style="display: none">
        <h1 class="heading">Upcoming Bids</h1>
        <div class="images-group">
            <img src="biryani.jpg"/>
            <img src="coffee.jpg" />
            <img src="mobile.jpg" />

        </div>
        <div class="images-group">
            <img src="tv.jpg" />
            <img src="watch.jpg" />
            <img src="jacket.jpg" />
        </div>
    </div>
    <div>
            <div id="myDiv3" style="display: none">
                    <h1 class="heading">Completed Bids</h1>
                    <div class="images-group">
                            <img src="biryani.jpg"/>
                        <img src="coffee.jpg" />
                        <img src="mobile.jpg" />
            
                    </div>
                    <div class="images-group">
                        <img src="tv.jpg" />
                        <img src="watch.jpg" />
                        <img src="jacket.jpg" />
                    </div>
        </div>
        <div>



    </div>
    </div>
    <p id="demo"></p>
    <script>
        // Set the date we're counting down to
        var countDownDate = new Date("Jan 1, 2019 15:37:25").getTime();

        // Update the count down every 1 second
        var x = setInterval(function () {

            // Get todays date and time
            var now = new Date().getTime();

            // Find the distance between now and the count down date
            var distance = countDownDate - now;

            // Time calculations for days, hours, minutes and seconds
            var days = Math.floor(distance / (1000 * 60 * 60 * 24));
            var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((distance % (1000 * 60)) / 1000);

            // Output the result in an element with id="demo"
            document.getElementById("demo").innerHTML = days + "d " + hours + "h "
                + minutes + "m " + seconds + "s ";

            // If the count down is over, write some text 
            if (distance < 0) {
                clearInterval(x);
                document.getElementById("demo").innerHTML = "EXPIRED";
            }
        }, 1000);

        /*function showHide(show, hide) {

        }
*/

        function hide(mydiv) {
            var x = document.getElementById("myDiv");
            var y = document.getElementById("myDiv2");
            var z = document.getElementById("myDiv3");
            if (mydiv=="div1" ) {

                x.style.display = "block";
                z.style.display="none"
                y.style.display = "none";
            
            }else if  (mydiv=="div2"){
            
                x.style.display = "none";
                y.style.display = "block";
                z.style.display='none'
            }
            else if  (mydiv=="div3"){
                x.style.display = "none";
                y.style.display = "none";
                z.style.display='block'}
            
        }



</script>



</body>

</html>
