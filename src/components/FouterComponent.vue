<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css">

    <footer>
        <div class="up-section">
            <a href="#" class="f-logo">Hamburger</a>

            <ul>
                <h1>Section</h1>
                <li><a href="#">Company</a></li>
                <li><a href="#">Location</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Our Services</a></li>
            </ul>

            <ul>
                <h1>Contact us</h1>
                <li><p>+1 123 456 7890</p></li>
                <br>
                <li><p>House #215, Street 5</p></li>
                <br>
                <li><p>Washignton, DC</p></li>
            </ul>
        </div>

        <div class="down-section">
            <ul>
                <h1>Support</h1>
                <li><a href="#">exemple.gmail.com</a></li>
            </ul>

            <div class="social">
                <h1>Social</h1>

                <div class="social-icons">
                    <a href="#"><i class="fa-brands fa-facebook"></i></a>
                    <a href="#"><i class="fa-brands fa-x-twitter"></i></a>
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-youtube"></i></a>
                </div>
            </div>

            <div class="search">
                <h1>Email</h1>

                <input type="email" placeholder="Enter your email">
            </div>
        </div>
    </footer>
</template>

<style>
footer { 
    background-color: #111111; 
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.f-logo {
    color: #FFFFFF;
    font-family: 'Turret Road';
    letter-spacing: 2px;
    padding: 5px 10px;
    font-size: 25px;
}

.up-section, .down-section {
    display: flex;
    justify-content: space-between;
    padding: 3% 0px;
    margin: 5px;
    width: 80%;
    flex-wrap: wrap;
}

.up-section { border-bottom: 1px solid #545562; }
.up-section ul li a:hover, .down-section ul li a:hover { color: #9A9FF6; }
.social-icons { display: flex; }

.up-section ul, 
.down-section ul { 
    font-family: 'Montserrat'; 
    margin: 0; 
    padding: 0 20px; 
}

.up-section ul li a, 
.down-section ul li a { 
    font-size: 16px; 
    color: #FFFFFF; 
    transition: all ease .5s; 
}

.up-section ul li p, 
.down-section ul li p { 
    font-size: 14px; 
    color: #FFFFFF; 
    line-height: 10px; 
    transition: all ease .5s; 
}

.up-section h1, .down-section h1 { 
    color: #9697A0; 
    font-size: 20px; 
    font-family: 'Montserrat'; 
}

.social-icons a { 
width: 35px;
height: 35px;
margin: 0 5px;
background-color: #636363;
box-shadow: 2px 2px 12px rgba(0, 0, 0, .1);
display: flex;
justify-content: center;
align-items: center;
transition: all ease .5s;
}

.social-icons a:hover { opacity: 0.5; }

.social-icons i { 
    color: #FFFFFF; 
    font-size: 14px; 

}
.social-icons a:hover i { color: #424356; }

.search input {
    height: 35px;
    width: 200px;
    text-align: center;
    border: none;
    outline: none;
}

@media(max-width: 1024px) {
    .search {
        margin: 20px auto;
        display: flex;
        align-items: center;
        width: 100%;
        justify-content: center; 
    }

    .search h1 { margin: 20px; }
}

@media(max-width: 820px) {
    body { background-color: #C03B3D; }
    .up-section ul h1, .down-section ul h1 { font-size: 25px; }

    .up-section, 
    .down-section { 
        flex-direction: column; 
        align-items: center; 
        text-align: center; 
    }

    .up-section ul li, 
    .down-section ul li { 
        text-align: center; 
        margin: 10px; 
    }
}

@media(max-width: 420px) {
    .search { flex-direction: column; }
    .copyright { font-size: 14px; }
    .f-logo { font-size: 16px; }
}
</style>
