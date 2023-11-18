<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Website</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&family=Montserrat:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="main">
        <div class="logo">
            <div class="text">
                <div class="hello">Hello there!<br>My name is</div>
                <div class="name">Tristan</div>
            </div>
            <img src="IMG_20230218_090242_866.png" class="image"></img>
        </div>
        <div class="scroll" onclick="scrollToTop()">
            <svg width="28" height="17" viewBox="0 0 28 17" fill="none" xmlns="http://www.w3.org/2000/svg" class="fleche">
                <path d="M2 2L14 14L26 2" stroke="#7C7C7C" stroke-width="4" stroke-linecap="round"/>
            </svg>
        </div>
        <div class="container">
            <div class="allgrad">
                <div class="blur"></div>
                <div class="gradien"></div>
            </div>
            <div class="content">
                <div class="infos">
                    <div class="age">Hi! I'm Tristan, a 17-year-old high school senior studying in the <a href="https://www.letudiant.fr/bac/qu-est-ce-qu-un-bac-sti2d.html">STI2D program</a>, with a passion for web development.<br>Originally from Paris, I dedicate myself with incredible motivation to various computing projects.<br> <br>Feel free to contact me through the links below for discussions or collaborations:
                    </div>
                </div>
                <div class="button">coucou</div>
                <div class="button">coucou</div>
            </div>
        </div>
    </div>
</body>
</html>

<script>
    function scrollToTop() {
            const currentScroll = document.documentElement.scrollTop || document.body.scrollTop;

            if (currentScroll > 300) {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            } else {
                window.scrollTo({
                    top: 600,
                    behavior: 'smooth'
                });
            }
        }
    
const parallaxImage = document.querySelector('.image');
const parallaxText = document.querySelector('.text');

function handleParallax() {
    const scrollPosition = window.scrollY;
    parallaxImage.style.transform = `translateY(-${scrollPosition * 0.2}px)`;
    parallaxText.style.transform = `translateY(-${scrollPosition * 0.3}px)`;
}
window.addEventListener('scroll', handleParallax);

</script>

<style>
  body {
    background-color: #303030;
    color: white;
    font-family: "Montserrat";
    font-weight: 400;
    font-size: 26px;
    margin: 0;
}

a {
    text-decoration: none;
    color: #00da00;
}

a:hover {
    text-decoration: underline;
}

.text {
    z-index: 6;
    opacity: 1;
    position: fixed;
    left: 10%;
    top: 10%;
}

.hello {
    font-weight: 400;
    color: #efefef;
}

.name {
    font-weight: 700;
    font-size: 46px;
}

.main {
    margin: auto;
    max-width: 1200px;
    padding: 20px 20px 20px 20px;
    height: 100%;
}

.logo {
    left: calc(6% - 40px);
    position: relative;
    height: 380px;
    width: 300px;
    justify-content: center;
    align-items: center;
}

.image {
    border-radius: 40px;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

@media (max-width: 840px) {

    .allgrad {
        position: relative;
        height: 100px;
    }

    .blur {
        width: 100%;
        height: 160%;
        position: absolute;
        overflow: visible;
        -webkit-mask: linear-gradient(to top,rgb(0, 0, 0), rgb(0, 0, 0), transparent);
        mask: linear-gradient(to top, black, black, transparent);
        -webkit-filter: blur(4px);
        filter: blur(4px);
        backdrop-filter: blur(4px);
        bottom: 0;
    }    

    .gradien {
        background: linear-gradient(0deg, rgb(0, 0, 0) 0%, rgba(255,255,255,0) 100%);
        height: 100px;
        width: 100%;
        position: absolute;
        bottom: 0;
    }

    .logo {
        position: fixed;
        left: 0;
        width: 100%;
    }

    .image {
        border-radius: 0;
        width: 100%;
        height: 100%;
        object-fit: cover; /* ajoute une transition pour un effet plus fluide */
    }

    .main {
        padding: 0;
    }

    .container {
        position: relative;
        top: 360px;
        z-index: 1;
    }

    body {
        background-color: black;
    }

    .content {
        padding: 20px;
        position: relative;
        background-color: rgb(0, 0, 0);
    }

    .scroll {
        cursor: pointer;
        z-index: 10;
        position: fixed;
        right: 6%;
        bottom: 6%;
        height: 38px;
        border-radius: 1000px;
        background-color: rgba(49, 49, 49, 0.5);
        backdrop-filter: blur(4px);

        width: 38px;
        align-items: center;
        justify-content: center;
        transition: all 0.2s ease;
    }

    .scroll:hover {
        transition: all 0.2s ease;
        background-color: rgba(71, 71, 71, 0.5);
    }

    .scroll:active {
        transition: all 0.2s ease;
        background-color: rgba(95, 95, 95, 0.5);
    }

    .button {
        cursor: pointer;
        background-color: #191919;
        color: #00da00;
        font-weight: 500;
        font-size: 18px;
        width: fit-content;
        margin-bottom: 20px;
        margin-left: 10px;
        padding: 8px 16px 8px 16px;
        border-radius: 1000px;
    }

    .fleche {
        position: relative;
        left: 50%;
        top: 50%;
        width: 24px;
        transform: translate(-50%, -85%);
    }

    #scroll.up {
        transform: rotate(180deg);
    }

    .age {
        font-size: 18px;
        font-weight: 400;
        color: rgb(255, 255, 255);
    }
}
</style>
