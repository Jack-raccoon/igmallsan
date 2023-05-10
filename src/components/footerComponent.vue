<template>
    <footer>
        <div class="footer__information">
            <div class="footer__logo">
                <img src="./../assets/logo.jpeg" alt="logo" />
            </div>
            <div class="information__address">
                <h3>Address</h3>
                <p>Av. Los Alamos 123</p>
                <p>San Juan de Lurigancho</p>
                <p>Lima - Perú</p>
            </div>
            <div class="information__contact">
                <h3>Contact</h3>
                <p>Celular: +51 990 460 089</p>
                <p>Email: LuisMallccoSanchez@igmallsan.onmicrosoft.com</p>
            </div>
        </div>
        <div class="copy">
            <!-- copyright -->
            <p>Inversiones Generales Mallsan</p>
            <p>© 2021 Todos los derechos reservados.</p>
        </div>
    </footer>
</template>

<style scoped>
    footer {
        width: 100%;
        background-color: #fff;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12);
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }

    .footer__information {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        margin-bottom: 30px;
    }

    .footer__logo img {
        height: 7rem;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .copy {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: hsl(221, 85%, 64%);
        color: #fff;
    }

    @media screen and (max-width: 768px) {
        footer {
            width: 100%;
            background-color: #fff;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12);
            display: flex;
            flex-direction: column;
            justify-content: space-around;
        }
        .footer__information {
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .information__address, .information__contact {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .copy {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: hsl(221, 85%, 64%);
            color: #fff;
        }
    }

    @media screen and (max-width: 480px) {
        
    }
</style>