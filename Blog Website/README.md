# CVIP-Food-Blog-website-using-Html-Css
objective:
 
*/ HTML /*
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>JD Dining</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"
        integrity="sha512-iBBXm8fW90+nuLcSKlbmrPcLa0OT92xO1BIsZ+ywDWZCvqsWgccV3gFoRBv0z+8dLJgyAHIhR35VZc2oM/gI1w=="
        crossorigin="anonymous" referrerpolicy="no-referrer"/>
       
</head>
<style>  
  @import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
  *,
  *::after,
  *::before {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
  }
  .html {
    font-size: 52.5%;
  }
  body {
    font-family: "Poppins", sans-serif;
  }
  .container {
    max-width: 1200px;
    width: 90%;
    margin: auto;
  }
  .btn {
    display: inline-block;
    padding: 0em 1.2em;
    text-decoration: none;
    border-radius: 50px;
    cursor: pointer;
    outline: none;
    margin-top: 1em;
    text-transform: uppercase;
    font-weight: small;
  }
  .btn-primary {
    color:black;
    background:skyblue;
  }
  .btn-primary:hover {
    background: #117964;
    transition: background 0.3 ease-in-out;
  }
  .navbar input[type="checkbox"],
  .navbar .hamburger-lines {
    display: none;
  }
  .navbar {
    box-shadow: 0px 5px 10px 0px #ebbcbc;
    position: fixed;
    width: 100%;
    background:whitesmoke;
    color: #000;
    opacity: 0.85;
    height: 50px;
    z-index: 12;
  }
  .navbar-container {
    display: flex;
    justify-content: space-between;
    height: 50px;
    align-items: center;
  }
  .menu-items {
    order: 2;
    display: flex;
  }
  .menu-items li {
    list-style: none;
    margin-left: 1.5rem;
    margin-bottom: 0.5rem;
    font-size: 1.2rem;
  }
  .menu-items a {
    text-decoration: none;
    color: #f88d13;
    font-weight: 500;
    transition: color 0.3s ease-in-out;
  }
  .menu-items a:hover {
    color: #30e0bd;
    transition: color 0.3s ease-in-out;
  }
  .logo {
    order: 1;
    font-size: 2.3rem;
    margin-bottom: 0.5rem;
  }
  .showcase-area {
    height: 50vh;
    background: linear-gradient(
    rgba(240, 240, 240, 0.144),
    rgba(255, 255, 255, 0.336)
  ),
  url("https://i.postimg.cc/zBF9hxHg/cover4.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .showcase-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
    font-size: 1.8rem;
  }
  .main-title {
    margin-top:17px;
    text-align: center;
    top : 25%;
  }
  .showcase-area h3{
      text-align: center;
      font-family: sans-serif;
      font-size: 20px;
      row-gap: 5em;
      color:black;
  }
  .showcase-area p{
    text-align: center;
    color: #f88d13;
  }
  #about {
    padding: 50px 0;
    background: #ffcb6a;
  }
  .about-wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #about h2 {
    font-size: 2.3rem;
  }
  #about p {
    font-size: 1.2rem;
    color: #f0f0f0;
  }
   #about .small {
    font-size: 1.2rem;
    color: #666;
    font-weight: 600;
  }
  .about-img {
    flex: 1 1 400px;
    padding: 30px;
    transform: translateX(150%);
    animation: about-img-animation 1s ease-in-out forwards;
  }
  @keyframes about-img-animation {
    100% {
      transform: translate(0);
    }
  }
  .about-text {
    flex: 1 1 400px;
    padding: 30px;
    margin: auto;
    transform: translate(-150%);
    animation: about-text-animation 1s ease-in-out forwards;
  }
   @keyframes about-text-animation {
    100% {
      transform: translate(0);
    }
  }
  .about-img img {
    display: block;
    height: 400px;
    max-width: 100%;
    margin: auto;
    object-fit: cover;
    object-position: right;
  }
  #food {
    padding: 5rem 0 10rem 0;
  }
  #food h2 {
    text-align: center;
    font-size: 2.5rem;
    font-weight: 400;
    margin-bottom: 40px;
    text-transform: uppercase;
    color:orange;
  }
  .food-container {
    display: flex;
    justify-content: space-between;
  }
  .food-container img {
    display: block;
    width: 100%;
    margin: auto;
    max-height: 350px;
    object-fit: cover;
    object-position: center;
  }
  .img-container {
    margin: 0 1rem;
    position: relative;
  }
  .img-content {
    position: absolute;
    top: 70%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0;
    z-index: 2;
    text-align: center;
    transition: all 0.3s ease-in-out 0.1s;
  }
  .img-content h3 {
    color: #fff;
    font-size: 2.2rem;
  }
  .img-content a {
    font-size: 1.2rem;
  }
  .img-container::after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.871);
    opacity: 0;
    z-index: 1;
  
    transform: scaleY(0);
    transform-origin: 100% 100%;
    transition: all 0.3s ease-in-out;
  }
  .img-container:hover::after {
    opacity: 1;
    transform: scaleY(1);
  }
  .img-container:hover .img-content {
    opacity: 1;
    top: 40%;
  }
  .food-menu-heading {
    text-align: center;
    font-size: 3.4rem;
    font-weight: 400;
    color:orange;
  }
  .food-menu-container {
    display: flex;
    flex-wrap: wrap;
    padding: 50px 0px 50px 0px;
    color:black;
  }
  .food-menu-container img {
    display: block;
    width: 300px;
    height: 300px;
    border-radius: 50%;
    object-fit: cover;
    object-position: center;
  }
  .food-menu-item {
    display: flex;
    flex: 1 1 600px;
    justify-content: space-evenly;
    margin-bottom: 3rem;
  }
  .food-description {
    margin: auto 1.5rem;
  }
  .font-title {
    font-size: 1.8rem;
    font-weight: 400;
    color: #444;
  }
  .food-description p {
    font-size: 1.4rem;
    color: #555;
    font-weight: 500;
  }
  .food-description .food-price {
    color: #117964;
    font-weight: 700;
  }
  #testimonials {
    padding: 6rem 0;
    background: gainsboro;
  }
  .testimonial-title {
    text-align: center;
    font-size: 2.8rem;
    font-weight: 400;
    color: orange;
  }
  .testimonial-container {
    display: block;
    justify-content: space-between;
    font-size: 1.4rem;
    padding: 1rex;
  }
  .testimonial-box .checked {
    color:green;
  }
  .testimonial-box .testimonial-text {
    margin: 1rem 0;
    color: #444;
    text-align:center;
  }
  .testimonial-box {
    text-align: center;
    padding: 1rem;
  }
  .customer-photo img {
    display: block;
    width: 150px;
    height: 150px;
    object-fit: cover;
    object-position: center;
    border-radius: 50%;
    margin: auto;
  }
  #contact {
    padding: 5rem 0;
    background: transparent;
  }
  .contact-container {
    display: flex;
    background:transparent;
  }
  .contact-img {
    width: 50%;
  }
  .contact-img img {
    display: block;
    height: 400px;
    width: 100%;
    object-position: center;
    object-fit: cover;
  }
  .form-container {
    padding: 1rem;
    width: 50%;
    margin: auto;
  }
  .form-container input {
    display: block;
    width: 100%;
    border: none;
    border-bottom: 2px solid #7a7777;
    padding: 1rem 0;
    box-shadow: none;
    outline: none;
    margin-bottom: 1rem;
    color:orange;
    font-weight: 500;
  }
  .form-container textarea {
    display: block;
    width: 100%;
    border: none;
    border-bottom: 2px solid #6b6868;
    color:orange;
    outline: none;
    padding: 1rem 0;
    resize: none;
  }
  .form-container h2 {
    font-size: 2.7rem;
    font-weight: 500;
    color: #444;
    margin-bottom: 1rem;
    margin-top: -1.2rem;
  }
  .form-container a {
    font-size: 1.3rem;
  }
  #footer h2 {
    text-align: center;
    font-size: 1.2rem;
    padding: 1.6rem;
    font-weight: 500;
    color:khaki;
    background: grey;
  }

</style>
<body>
  <nav class="navbar">
    <div class="navbar-container container">
        <input type="checkbox" name="" id="">
        <div class="hamburger-lines">
            <span class="line line1"></span>
            <span class="line line2"></span>
            <span class="line line3"></span>
        </div>
<ul class="menu-items">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#food">Category</a></li>
                <li><a href="#food-menu">Menu</a></li>
                <li><a href="#testimonials">Testimonial</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <h1 class="logo">JD-F</h1>
        </div>
    </nav>
    <section class="showcase-area" id="showcase">
        <div class="showcase-container">
            <h3 class="main-title" id="home">Welcome to JD Dining</h3><br>
                <h3>"Flavourful Journeys on Every Plate"</h3>
            <p>>>Smell it>>Eat it>>Taste it>>Smile it>></p>
            <a href="#food-menu" class="btn btn-primary">Menu</a>
        </div>
    </section>

    <section id="about">
        <div class="about-wrapper container">
            <div class="about-text">
                <p class="small">About Us</p>
                <h2>We've been making healthy food for last 10 years and Serving with Love:) </h2>
                <p>
                  Starting Our journey in the kitchen, we're here to inspire and 
                  serve you with delicious recipes and joy of food.Let's eat,
                  taste and savor every moment Together! And make memories with
                  our Blogging.
                </p>
            </div>
            <div class="about-img">
                <img src="C:\Users\LENOVO\Desktop\Blog Website\img\about.jpeg" alt="food" width="320px" height="320px"/>
            </div>
        </div>
    </section>
    <section id="food">
        <h2>Special Food in Our Restaurnt </h2>
        <div class="food-container container">
            <div class="food-type Idly">
                <div class="img-container">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\mini idly.jpg" alt="error" />
                    <div class="img-content">
                        <h3>Mini Idly</h3>
                        <a href="https://en.wikipedia.org/wiki/Idli" class="btn btn-primary" target="blank">learn
                            more</a>
                    </div>
                </div>
            </div>
            <div class="food-type Rice">
                <div class="img-container">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\mango rice.jpg" alt="error" />
                    <div class="img-content">
                        <h3>Mango Rice</h3>
                        <a href="https://en.wikipedia.org/wiki/Mango_sticky_rice" class="btn btn-primary" target="blank">learn
                            more</a>
                    </div>
                </div>
            </div>
    </section>
    <section id="food-menu">
        <h2 class="food-menu-heading">Food Menu</h2>
        <div class="food-menu-container container">
            <div class="food-menu-item">
                <div class="food-img">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\Briyani.jpeg" alt="briyani" width="150px" height="150px" />
                </div>
                <div class="food-description">
                    <h2 class="food-titile">Briyani</h2>
                    <p> <h4>Added</h4>
                      Chicken biryani includes chicken, 
                      basmati rice, onions, tomatoes, garlic, ginger, yogurt,
                      and a blend of spices like cumin, coriander, turmeric, and garam masala.
                    </p>
                    <p class="food-price">Price: &#8377; 150Rs</p>
                </div>
            </div>

            <div class="food-menu-item">
                <div class="food-img">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\tandoori.jpg" alt="error" />
                </div>
                <div class="food-description">
                    <h2 class="food-titile">Tandoori</h2>
                    <p><h4>Added</h4>
                      Tandoori includes Cumin, coriander, turmeric, garam masala, and chili powder are all commonly used spices. 
                    </p>
                    <p class="food-price">Price: &#8377; 180Rs</p>
                </div>
            </div>
            <div class="food-menu-item">
                <div class="food-img">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\Garlic naan.jpg" alt="" />
                </div>
                <div class="food-description">
                    <h2 class="food-titile">Garlic Naan</h2>
                    <p><h4>Added</h4>
                      Garlic Naan makes from flour, yeast (or sometimes baking powder), yogurt, and a pinch of salt. 
                      Minced garlic or garlic paste is incorporated into the dough or spread on top before baking.
                    </p>
                    <p class="food-price">Price: &#8377; 85Rs</p>
                </div>
            </div>
            <div class="food-menu-item">
                <div class="food-img">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\chicken fry.jpg" alt="" />
                </div>
                <div class="food-description">
                    <h2 class="food-titile">Chicken Fry</h2>
                    <p><h4>Added</h4>
                        Chicken Fry includes chicken pieces in a blend of spices, herbs, 
                        and sometimes buttermilk or yogurt.
                        spices such as paprika, garlic powder, onion powder, cumin, coriander, and chili powder.
                    </p>
                    <p class="food-price">Price: &#8377; 200Rs</p>
                </div>
            </div>
            <div class="food-menu-item">
                <div class="food-img">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\south meal.jpg" alt="" />
                </div>
                <div class="food-description">
                    <h2 class="food-titile">South Meals</h2>
                    <p><h4>Added</h4>
                      South Indian meals include coconut chutney, sambar, rasam, and yogurt.
                      These dishes provide complementary flavors and textures to the meal.
                    </p>
                    <p class="food-price">Price: &#8377; 100Rs</p>
                </div>
            </div>
            <div class="food-menu-item">
                <div class="food-img">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Recipe img\Fish fry.jpg" alt="" />
                </div>
                <div class="food-description">
                    <h2 class="food-titile">Fish Fry</h2>
                    <p><h4>Added</h4>
                      Fish Fry includes whole fish with a mixture of spices, flour, or breadcrumbs, and then frying them in oil.
                     ingredients like turmeric, cumin, coriander, chili powder, and salt. 
                    </p>
                    <p class="food-price">Price: &#8377; 220Rs</p>
                </div>
            </div>
        </div>
    </section>
    <section id="testimonials">
        <h2 class="testimonial-title">What Our Customers Say</h2>
        <div class="testimonial-container container">
            <div class="testimonial-box">
                <div class="customer-detail">
                    <div class="customer-photo">
                        <img src="C:\Users\LENOVO\Desktop\Blog Website\Customer images\sathy.png" alt="" />
                        <p class="customer-name">Sathyaseelan</p>
                    </div>
                </div>
                <div class="star-rating">
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                </div>
                <p class="testimonial-text">
                    I'm Sathyaseelan. I liked this restaurant for Good ambiance and presentation of Food.
                    and I ate Chicken Briyani From this restaurant it was awesome and lit more Spicy but I really 
                    like this taste of the food here.
                </p>

            </div>
            <div class="testimonial-box">
                <div class="customer-detail">
                    <div class="customer-photo">
                        <img src="C:\Users\LENOVO\Desktop\Blog Website\Customer images\vikash.png" alt="" />
                        <p class="customer-name">Vikhash</p>
                    </div>
                </div>
                <div class="star-rating">
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                </div>
                <p class="testimonial-text">
                    Hi everyone, I have to share my opinion of this restaurant food.
                    last time i went to Coimbatore and that time i saw this restaurant
                    near Info college and I went there and taste the food from JD-Dining 
                    and I ordered Tandoori,it was so tasty and spicy to eat and I liked the way
                    of serving in the  JD-Dining.
                </p>

            </div>
            <div class="testimonial-box">
                <div class="customer-detail">
                    <div class="customer-photo">
                        <img src="C:\Users\LENOVO\Desktop\Blog Website\Customer images\siva.png" alt="" />
                        <p class="customer-name">Sivasubramanian</p>
                    </div>
                </div>
                <div class="star-rating">
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                    <span class="fa fa-star checked"></span>
                </div>
                <p class="testimonial-text">
                  Excellent customer service and a pleasant ambiance and Offering price also less in this restaurant.
                </p>
        </div>
        <div class="testimonial-box">
            <div class="customer-detail">
                <div class="customer-photo">
                    <img src="C:\Users\LENOVO\Desktop\Blog Website\Customer images\mano.png" alt="" />
                    <p class="customer-name">Manoj Kumar</p>
                </div>
            </div>
            <div class="star-rating">
                <span class="fa fa-star checked"></span>
                <span class="fa fa-star checked"></span>
                <span class="fa fa-star checked"></span>
                <span class="fa fa-star checked"></span>
            </div>
            <p class="testimonial-text">
              I visited this restaurant once and I got shocked from offering price of food. 
              And my shares about food is exceptional flavors, creative dishes, and good service.
            </p>
        </div>
    </section>
    <section id="contact">
        <div class="contact-container container">
            <div class="contact-img">
                <img src="C:\Users\LENOVO\Desktop\Blog Website\img\contact.jpg" alt="contact" />
            </div>

            <div class="form-container">
                <h2>Contact Us</h2>
                <input type="text" placeholder="Your Name" />
                <input type="email" placeholder="E-Mail" />
                <textarea cols="30" rows="6" placeholder="Type Your Message"></textarea>
                <a href="#" class="btn btn-primary">Submit</a>
            </div>
        </div>
    </section>
    <footer id="footer">
        <h2>JD-F &copy; all rights reserved</h2>
    </footer>

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script src="app.js"></script>



</body>
</html>