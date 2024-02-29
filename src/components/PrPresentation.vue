<template>
    <div class="presentation">
        <div class="photo">
            <img src="" alt="">
        </div>
        <div class="information">
            <h3>Alejandra Pantoja</h3>
            <p>Ux Writer</p>
            <p><a href="tel:+573003679301">+57 3003679301</a></p>
            <p>
                <a href="http://">
                    <span>Be</span>
                    <span>Malejapg</span>
                </a>
            </p>
        </div>
    </div>
</template>

<style scoped>
    .presentation {
        display: flex;
    }
    .photo {
        width: 90px;
        height: 100px;
        border-radius: 12px;
        background-color: black;
        margin-right: 20px;
    }
    .information h3{
        font-weight: 700;
        font-size: 18px;
        line-height: 21px;
        color: black;
    }
    .information p {
        font-weight: 400;
        font-size: 15px;
        line-height: 18px;
        color: #7C7C7C;
    }
    .information p a {
        text-decoration: none;
        color: unset;
    }
    .information p a:hover {
        text-decoration: underline;
        color: #1814EF;
    }
</style>