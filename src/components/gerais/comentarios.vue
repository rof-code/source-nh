<template>
    <section class="comentarios">
        <div class="container">
            <div class="row">
                <div class="col-sm-6 quemComprou">
                    <div class="titleSection">
                        <img src="@/assets/img/STAR.png" alt="">
                        <h1>PORQUE ESCOLHER A <br>
                        <span>NEW HAIR?</span></h1>
                    </div>

                    <h3>Quem comprou conta.</h3>
                    <p>
                        Com produtos reconhecidos no mercado, a New Hair <br class="desk">
                        preza pelo seu bem-estar de maneira leve e saudável. <br class="desk">
                        100% natural e sem testar em animais, somos o <br class="desk">
                        blend de vitaminas Nº1 do Brasil, ideal para quem <br class="desk">
                        deseja recuperar a autoestima e os cuidados com as <br class="desk">
                        madeixas. 
                        <br class="desk"><br class="desk">
                        Fórmula poderosa para quem merece um tratamento <br class="desk">
                        poderoso. #lovenewhair
                    </p>
                </div>
                <div class="col-sm-6 colComents">
                    <div class="col-sm-12 d-flex contentBox">
                        <div class="col-sm-12 authorBox">
                            <div class="row justify-content-evenly">
                                <div class="col-2">
                                    <img src="@/assets/img/yeda.png" alt="">
                                </div>
                                <div class="col-4">
                                    <div class="author">
                                        <p>Yeda Andrade</p>
                                        <span>@yedanascentes</span> <br >
                                        <span>Comprador verificado</span>
                                    </div>
                                </div>
                                <div class="col-3">
                                  <img src="@/assets/img/star_com.png" alt="">
                                </div>
                                <div class="col-1">
                                    <a href="https://www.instagram.com/yedanascentes" target="_blank">
                                        <img src="@/assets/img/insta_com.png" alt="">
                                    </a>
                                </div>
                                <p class="comentBox">
                                    É muito bom, estou tomando e meus cabelos pararam de cair! Está <br class="desk">
                                    com muito brilho e super recomendo! 
                                </p>
                            </div><!--row-->
                        </div><!--col-sm-12-author-->
                    </div><!--contentBox-->

                    <div class="col-sm-12 d-flex contentBox">
                        <div class="col-sm-12 authorBox">
                            <div class="row justify-content-evenly">
                                <div class="col-2">
                                    <img src="@/assets/img/isa.png" alt="">
                                </div>
                                <div class="col-4">
                                    <div class="author">
                                        <p>Isabelle Oliveira</p>
                                        <span>@isabelleoliveira05</span> <br>
                                        <span>Comprador verificado</span>
                                    </div>
                                </div>
                                <div class="col-3">
                                  <img src="@/assets/img/star_com.png" alt="">
                                </div>
                                <div class="col-1">
                                    <a href="https://www.instagram.com/isabelleoliveira05" target="_blank">
                                        <img src="@/assets/img/insta_com.png" alt="">
                                    </a>
                                </div>
                                <p class="comentBox">
                                    Genteeee eu preciso contar a minha experiência. Meu cabelo caia <br class="desk">
                                    demais, eu trabalho de home office e mesmo sentada sem mexer nele, <br class="desk">
                                    no final do dia o chão estava cheio de cabelo, no travesseiro, se eu <br class="desk">
                                    mexesse no cabelo então, vinha vários fios na minha mão. E pasmem, <br class="desk">
                                    estou tomando o New Hair somente há uma semana e o chão está <br class="desk">
                                    limpo, meu travesseiro limpo de cabelo e passo a mão e não cai nem <br class="desk">
                                    um fio. Tô feliz demais e super indico!!!!
                                </p>
                            </div><!--row-->
                        </div><!--col-sm-12-author-->
                    </div><!--contentBox-->

                    <div class="col-sm-12 d-flex contentBox">
                        <div class="col-sm-12 authorBox">
                            <div class="row justify-content-evenly">
                                <div class="col-2">
                                    <img src="@/assets/img/paty.png" alt="">
                                </div>
                                <div class="col-4">
                                    <div class="author">
                                        <p>Paty Ribeiro</p>
                                        <span>@patricia.candida.986</span> <br>
                                        <span>Comprador verificado</span>
                                    </div>
                                </div>
                                <div class="col-3">
                                  <img src="@/assets/img/star_com.png" alt="">
                                </div>
                                <div class="col-1">
                                    <a href="https://www.instagram.com/patricia.candida.986" target="_blank">
                                        <img src="@/assets/img/insta_com.png" alt="">
                                    </a>
                                </div>
                                <p class="comentBox">
                                    Gente, sem igual! Estou tomando por indicação de uma amiga, eu já <br class="desk">
                                    estava praticamente careca, faz 2 meses que comecei a tomar, é <br class="desk">
                                    incrível como já nasceu cabelos.
                                </p>
                            </div><!--row-->
                        </div><!--col-sm-12-author-->
                    </div><!--contentBox-->
                    
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.comentarios{
    padding:30px 0px;
    .titleSection{
        h1{
            font-family: 'Poppins',sans-serif;
            color:#404040;
            font-weight: 900;
            font-size:50px;
            margin-top: 15px;
            line-height: 50px;
        }
        h1 span{
            color: #FFF;
            -webkit-text-stroke-width: 1px;
            -webkit-text-stroke-color: #000;
        }
    }
    .quemComprou{
        padding-left:28px;
        h3{
            color:#404040;
            font-family: 'Poppins',sans-serif;
            font-weight: 900;
            font-size:30px;
            margin-top:30px
        }
        p{
            color:#666666;
            font-family: 'Roboto',sans-serif;
            font-weight: 300;
            font-size: 19px;
            line-height: 21px;
            margin-top:20px;
        }
    }
    .colComents{
        .col-sm-12{
            background-color:#f1f1f1;
        }
    }
}
.contentBox{
    padding:15px 0px;
    margin:20px 0px;
}
.author{
    font-family:'Roboto',sans-serif;
    p:first-child{
        color:#404040;
        font-weight:bold;
        font-size:15px;
    }
    span:nth-of-type(1){
        color:#666666;
        font-weight:300;
        font-size:14px;
    }
    span:nth-of-type(2){
        font-size:13px;
        color:#5acc8a;

    }
}
.authorBox{
    font-family: 'Roboto',sans-serif;
    .col-2{
        padding-left: 0;
    }
    .col-4{
        position:relative;
        left:-9%;
    }
    .col-3{
        position:relative;
        left:-20%;
    }
    .col-1 img{
        max-width:28px !important;
        height:28px !important;
    }
    .comentBox{
        font-family: 'Roboto',sans-serif;
        font-size:15px;
        font-weight:300;
        color:#666666;
        line-height:16px;
        margin-top:10px;
        padding-left:20px;
    }
}

@media screen and (max-width:800px){
    .authorBox{
        .col-4{
            width:40%;  
            left:-7%;
            .author{
                p{
                    font-size: 14px;
                }
            }

        }
        .col-3{
            left:-15%;
        }
        .col-1{
            position:relative;
            left:-5%;
        }
        .col-2{
            display: flex;
            align-items: center;
            justify-content: center;
        }
    }
    .author{
        span:last-child{
            font-size:11px;
        }
        
    }
    .comentarios .quemComprou{
        padding-left: 12px;
    }
}

</style>