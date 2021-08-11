<template>
    <section class="produtosBox">
        <div class="container boxContainer">
            <div class="titleSection text-center">
                <h1>ESCOLHA AGORA SEU KIT</h1>
                <p>Cabelo sem queda, com mais brilho, força e muito crescimento</p>
            </div>
            <div class="trocaProduto">
                <div class="row justify-content-center">
                    <div class="col-12 d-flex escolhas" style="padding:0px 6px;">
                        <div class="col-6 col-sm-4">
                            <div class="col-12 produtoAtivo btn1" id="btn1">
                                <p>GUMMIES</p>
                                <span class="whiteLine activeLine"></span>
                            </div>
                        </div>
                        <div class="col-6 col-sm-4">
                            <div class="col-12 btn2" id="btn2">
                                <p>CÁPSULAS</p>
                                <span class="whiteLine"></span>
                            </div>
                        </div>
                        <div class="col-sm-4 desk">
                            <div class="col-12 btn3" id="btn3">
                                <p>HIDRATAÇÃO</p>
                                <span class="whiteLine"></span>
                            </div>
                        </div>
                    </div>
                </div>
            </div><!--troca produto-->

            <div class="row gummiesRow" id="gummiesRow">
                <div class="col-sm-6">
                    <div class="col-12 d-flex colCentral" id="gummies30">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>20% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies30.png" style="margin:35px 0px 20px 0px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>1 mês de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR GUMMIES <br>
                               (NOVO)</p>
                                <span><s style="color:#8f8f8f;">R$ 149,90</s>  R$ 119,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 9,99</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra" @click="addCartBoxCompra();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral" id="gummies180">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>55% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies180.png" style="max-width:90%;margin:50px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 6 GANHE BRINDE</p>
                                <p>6 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>6 POTES NEW HAIR GUMMIES <br>
                               + MASSAGEADOR + MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 899,40</s>  R$ 399,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 33,32</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra2();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral" id="nh90">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>37% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair90.png" style="margin:40px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 3 E GANHE BRINDE</p>
                                <p>3 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>3 POTES NEW HAIR CAPS<br>
                               + BRINDE MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 359,70</s>  R$ 227,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 18,97</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra4();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral" id="nh12">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>55% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair12.png" style="max-width:90%;margin:50px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 12 E GANHE BRINDE</p>
                                <p>12 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>12 POTES NEW HAIR CAPS <br>
                               + BRINDE KIT HIDRATAÇÃO</p>
                                <span><s style="color:#8f8f8f;">R$ 1.438,80</s>  R$ 627,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 52,31</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"   @click="addCartBoxCompra6();">
                           </div>
                       </div>
                    </div><!--col-central-->
                    
                    <!--MASCARA-->
                    <div class="col-12 d-flex colCentral" id="mask">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>19% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/mask.png" style="margin:80px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Máscara Capilar Hidratação Intensa</p>
                           </div>
                           <div class="productForm">
                               <p>New Hair MÁSCARA CAPILAR <br>
                               HIDRATAÇÃO INTENSA - 250G</p>
                                <span><s style="color:#8f8f8f;">R$ 119,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"   @click="addCartBoxCompra7();">
                           </div>
                       </div>
                    </div> 
                    

                </div><!--col-6-divisor-->


                <!--coluna-6-divisor-->
                <div class="col-sm-6">

                    <div class="col-12 d-flex colCentral"  id="gummies90">
                       <div class="crono" style="background-color:#fffc00;color:#ff2c7b;position:absolute;top:-45px;width:100%;text-align:center;padding:10px 30px;">
                            <p style="font-weight:bold;">OFERTA EXPIRA EM: <span id="crono"></span></p>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>37% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies90.png" style="margin:40px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 3 E GANHE BRINDE</p>
                                <p>3 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>3 POTES NEW HAIR GUMMIES <br>
                               + BRINDE MASSAGEADOR</p>
                                <span><s style="color:#8f8f8f;">R$ 449,70</s>  R$ 279,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 23,32</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra1();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <!--30dias caps-->
                    <div class="col-12 d-flex colCentral" id="nh30">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>19% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair30.png" style="margin:40px 0px 35px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>1 mês de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR CAPS<br>
                               VITAMIN</p>
                                <span><s style="color:#8f8f8f;">R$ 119,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra" @click="addCartBoxCompra3();">
                           </div>
                       </div>
                    </div>  



                    <!-- KIT180 CAPS-->
                    <div class="col-12 d-flex colCentral" id="nh180">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>54% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair180.png" style="max-width:90%;margin:35px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 6 E GANHE BRINDE</p>
                                <p>6 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>6 POTES NEW HAIR CAPS<br>
                               + MASSAGEADOR + MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 714,00</s>  R$ 327,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 27,31</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra5();">
                           </div>
                       </div>
                    </div><!--col-central--> 


                    <!--LISO-EXTREMO-->
                    <div class="col-12 d-flex colCentral" id="liso">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>9% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/liso.png" style="max-width:235px; max-height:227px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.8%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Liso Extremo Fluido Termoativado</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR LISO EXTREMO <br>
                               FLUIDO TERMOATIVADO - 120ML</p>
                                <span><s style="color:#8f8f8f;">R$ 139,90</s>  R$ 127,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 10,64</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra" @click="addCartBoxCompra8();">
                           </div>
                       </div>
                    </div>


                    <!--SHAMPOO-->
                     <div class="col-12 d-flex colCentral" id="shampoo">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>25% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/shampoo.png" style="margin:38px 0px 15px 0px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Kit  Shampoo + Condicionador</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR SHAMPOO - 250ML <br>
                               NEW HAIR CONDICIONADOR - 250ML</p>
                                <span><s style="color:#8f8f8f;">R$ 129,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra9();">
                           </div>
                       </div>
                    </div> 

                </div><!--col-6-divisor-->
            </div><!--gummiesRow-->



            <div class="row capsRow align-items-center" id="capsRow">
                <div class="col-sm-6">
                 <!--30dias caps-->
                    <div class="col-12 d-flex colCentral" id="nh30">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>19% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair30.png" style="margin:40px 0px 35px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>1 mês de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR CAPS<br>
                               VITAMIN</p>
                                <span><s style="color:#8f8f8f;">R$ 119,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"   @click="addCartBoxCompra3();">
                           </div>
                       </div>
                    </div> 


                     <!-- KIT180 CAPS-->
                    <div class="col-12 d-flex colCentral" id="nh180">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>54% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair180.png" style="max-width:90%;margin:35px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 6 E GANHE BRINDE</p>
                                <p>6 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>6 POTES NEW HAIR CAPS<br>
                               + MASSAGEADOR + MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 714,00</s>  R$ 327,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 27,31</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra5();">
                           </div>
                       </div>
                    </div><!--col-central--> 

                    <div class="col-12 d-flex colCentral" id="gummies30">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>20% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies30.png" style="margin:35px 0px 20px 0px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>1 mês de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR GUMMIES <br>
                               (NOVO)</p>
                                <span><s style="color:#8f8f8f;">R$ 149,90</s>  R$ 119,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 9,99</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral" id="gummies180">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>55% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies180.png" style="max-width:90%;margin:50px 0px 25px 0px;" alt="">
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 6 GANHE BRINDE</p>
                                <p>6 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>6 POTES NEW HAIR GUMMIES <br>
                               + MASSAGEADOR + MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 899,40</s>  R$ 399,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 33,32</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra2();">
                           </div>
                       </div>
                    </div><!--col-central-->
                    
                    <!--MASCARA-->
                    <div class="col-12 d-flex colCentral" id="mask">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>19% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/mask.png" style="margin:80px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Máscara Capilar Hidratação Intensa</p>
                           </div>
                           <div class="productForm">
                               <p>New Hair MÁSCARA CAPILAR <br>
                               HIDRATAÇÃO INTENSA - 250G</p>
                                <span><s style="color:#8f8f8f;">R$ 119,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra" @click="addCartBoxCompra7();">
                           </div>
                       </div>
                    </div> 
                    

                </div><!--col-6-divisor-->


                <!--coluna-6-divisor-->
                <div class="col-sm-6">
                    <div class="col-12 d-flex colCentral" id="nh90">
                        <div class="crono" style="background-color:#fffc00;color:#ff2c7b;position:absolute;top:-45px;width:100%;text-align:center;padding:10px 30px;">
                            <p style="font-weight:bold;">OFERTA EXPIRA EM: <span id="crono1"></span></p>
                        </div>
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>37% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair90.png" style="margin:40px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 3 E GANHE BRINDE</p>
                                <p>3 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>3 POTES NEW HAIR CAPS<br>
                               + BRINDE MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 359,70</s>  R$ 227,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 18,97</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra4();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral" id="nh12">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>55% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair12.png" style="max-width:90%;margin:50px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 12 E GANHE BRINDE</p>
                                <p>12 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>12 POTES NEW HAIR CAPS <br>
                               + BRINDE KIT HIDRATAÇÃO</p>
                                <span><s style="color:#8f8f8f;">R$ 1.438,80</s>  R$ 627,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 52,31</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"   @click="addCartBoxCompra6();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral"  id="gummies90" >
                      
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>37% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies90.png" style="margin:40px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 3 E GANHE BRINDE</p>
                                <p>3 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>3 POTES NEW HAIR GUMMIES <br>
                               + BRINDE MASSAGEADOR</p>
                                <span><s style="color:#8f8f8f;">R$ 449,70</s>  R$ 279,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 23,32</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra1();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <!--LISO-EXTREMO-->
                    <div class="col-12 d-flex colCentral" id="liso">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>9% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/liso.png" style="max-width:235px; max-height:227px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.8%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Liso Extremo Fluido Termoativado</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR LISO EXTREMO <br>
                               FLUIDO TERMOATIVADO - 120ML</p>
                                <span><s style="color:#8f8f8f;">R$ 139,90</s>  R$ 127,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 10,64</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra8();">
                           </div>
                       </div>
                    </div>


                    <!--SHAMPOO-->
                     <div class="col-12 d-flex colCentral" id="shampoo">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>25% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/shampoo.png" style="margin:38px 0px 15px 0px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Kit  Shampoo + Condicionador</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR SHAMPOO - 250ML <br>
                               NEW HAIR CONDICIONADOR - 250ML</p>
                                <span><s style="color:#8f8f8f;">R$ 129,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra9();">
                           </div>
                       </div>
                    </div> 

                </div><!--col-6-divisor-->
            </div><!--capsRow-->

            <div class="row hidroRow">
                <div class="col-sm-6">
                     <!--LISO-EXTREMO-->
                    <div class="col-12 d-flex colCentral">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>9% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/liso.png" style="max-width:235px; max-height:227px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.8%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Liso Extremo Fluido Termoativado</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR LISO EXTREMO <br>
                               FLUIDO TERMOATIVADO - 120ML</p>
                                <span><s style="color:#8f8f8f;">R$ 139,90</s>  R$ 127,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 10,64</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra8();">
                           </div>
                       </div>
                    </div>

                    <!--MASCARA-->
                    <div class="col-12 d-flex colCentral">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>19% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/mask.png" style="margin:80px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Máscara Capilar Hidratação Intensa</p>
                           </div>
                           <div class="productForm">
                               <p>New Hair MÁSCARA CAPILAR <br>
                               HIDRATAÇÃO INTENSA - 250G</p>
                                <span><s style="color:#8f8f8f;">R$ 119,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra" @click="addCartBoxCompra7();">
                           </div>
                       </div>
                    </div> 

                    <div class="col-12 d-flex colCentral" style="margin-top:65px;" id="gummies90">
                       <div class="crono" style="background-color:#fffc00;color:#ff2c7b;position:absolute;top:-45px;width:100%;text-align:center;padding:10px 30px;">
                            <p style="font-weight:bold;">OFERTA EXPIRA EM: <span id="crono2"></span></p>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>37% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies90.png" style="margin:40px 0px 20px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 3 E GANHE BRINDE</p>
                                <p>3 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>3 POTES NEW HAIR GUMMIES <br>
                               + BRINDE MASSAGEADOR</p>
                                <span><s style="color:#8f8f8f;">R$ 449,70</s>  R$ 279,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 23,32</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra1();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <!--30dias caps-->
                    <div class="col-12 d-flex colCentral" id="nh30">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>19% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair30.png" style="margin:40px 0px 35px 0px" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>1 mês de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR CAPS<br>
                               VITAMIN</p>
                                <span><s style="color:#8f8f8f;">R$ 119,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra3();">
                           </div>
                       </div>
                    </div> 

                     <!-- KIT180 CAPS-->
                    <div class="col-12 d-flex colCentral">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>54% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair180.png" style="max-width:90%;margin:35px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 6 E GANHE BRINDE</p>
                                <p>6 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>6 POTES NEW HAIR CAPS<br>
                               + MASSAGEADOR + MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 714,00</s>  R$ 327,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 27,31</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"   @click="addCartBoxCompra5();">
                           </div>
                       </div>
                    </div><!--col-central-->  
                </div><!--col-6-divisor-->


                <!--coluna-6-divisor-->
                <div class="col-sm-6">
                    <!--SHAMPOO-->
                     <div class="col-12 d-flex colCentral">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>25% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/shampoo.png" style="margin:38px 0px 15px 0px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>Kit  Shampoo + Condicionador</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR SHAMPOO - 250ML <br>
                               NEW HAIR CONDICIONADOR - 250ML</p>
                                <span><s style="color:#8f8f8f;">R$ 129,90</s>  R$ 97,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 8,14</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra9();">
                           </div>
                       </div>
                    </div> 

                    <div class="col-12 d-flex colCentral">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>20% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies30.png" style="margin:35px 0px 20px 0px;" class="imgResponsive" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:20%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 1</p>
                                <p>1 mês de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>1 POTE NEW HAIR GUMMIES <br>
                               (NOVO)</p>
                                <span><s style="color:#8f8f8f;">R$ 149,90</s>  R$ 119,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 9,99</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra();">
                           </div>
                       </div>
                    </div><!--col-central-->


                    <div class="col-12 d-flex colCentral">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox">
                               <p>55% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/gummies180.png" style="max-width:90%;margin:50px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 6 GANHE BRINDE</p>
                                <p>6 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>6 POTES NEW HAIR GUMMIES <br>
                               + MASSAGEADOR + MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 899,40</s>  R$ 399,90</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 33,32</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra2();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral" id="nh90">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>37% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair90.png" style="margin:40px 0px 20px 0px" class="imgResponsive" alt="">
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 3 E GANHE BRINDE</p>
                                <p>3 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>3 POTES NEW HAIR CAPS<br>
                               + BRINDE MÁSCARA</p>
                                <span><s style="color:#8f8f8f;">R$ 359,70</s>  R$ 227,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 18,97</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"  @click="addCartBoxCompra4();">
                           </div>
                       </div>
                    </div><!--col-central-->

                    <div class="col-12 d-flex colCentral">
                       <div class="col-sm-6 p-0">
                           <div class="descontoBox capBox">
                               <p>55% DE DESCONTO</p>
                           </div>
                           <div class="imgBox">
                               <img src="@/assets/img/newhair12.png" style="max-width:90%;margin:50px 0px 25px 0px;" alt="">
                               <div class="flag" style="width:50%;background-color:#fffc00;position:absolute;top:0;left:0;padding:10px 20px;top:19.2%;">
                                   <p style="font-family:'Roboto',sans-serif;font-weight:900;font-size:14px;">FRETE GRÁTIS</p>
                               </div>
                           </div>
                       </div>
                       <div class="col-sm-6 p-0">
                           <div class="titleBox">
                                <p>COMPRE 12 E GANHE BRINDE</p>
                                <p>12 meses de tratamento</p>
                           </div>
                           <div class="productForm">
                               <p>12 POTES NEW HAIR CAPS <br>
                               + BRINDE KIT HIDRATAÇÃO</p>
                                <span><s style="color:#8f8f8f;">R$ 1.438,80</s>  R$ 627,70</span>
                                <p>Ou 12x sem juros de</p>
                                <span class="price">R$ 52,31</span>
                                <input type="submit" value="COMPRE AGORA" class="btnCompra"   @click="addCartBoxCompra6();">
                           </div>
                       </div>
                    </div><!--col-central-->

                </div><!--col-6-divisor-->
            </div><!--hidroRow-->
        </div>
    </section>
</template>

<script>
import Comunicacao from '@/comunicacao.js'
import $ from 'jquery';
export default {
    mounted(){
        // CRONOMETRO
        // Set the date we're counting down to
        var countDownDate = new Date("jan 29, 2022 23:59:59").getTime();
        // Update the count down every 1 second
        var x = setInterval(function() {
        // Get today's date and time
        var now = new Date().getTime();
        // Find the distance between now and the count down date
        var distance = countDownDate - now;
        // Time calculations for days, hours, minutes and seconds
        var days = Math.floor(distance / (1000 * 60 * 60 * 24));
        var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        var seconds = Math.floor((distance % (1000 * 60)) / 1000);
        var daybr = days;
        console.log(daybr);
        const textoHoras = (`00${hours}`).slice(-2);
        const textoMinutos = (`00${minutes}`).slice(-2);
        const textosegundos = (`00${seconds}`).slice(-2);

        // Display the result in the element with id="demo"
        document.getElementById("crono").innerHTML = textoHoras + ":"
        + textoMinutos + ":" + textosegundos;

        document.getElementById("crono1").innerHTML = textoHoras + ":"
        + textoMinutos + ":" + textosegundos;

        document.getElementById("crono2").innerHTML = textoHoras + ":"
        + textoMinutos + ":" + textosegundos;

        // If the count down is finished, write some text
        if (distance < 0) {
            clearInterval(x);
            document.getElementById("demo").innerHTML = "EXPIRED";
        }
        }, 1000);
        // CRONOMETRO

        // Troca de bloco de produtos
        $('#btn1').on('click', function(){
        $('.gummiesRow').css('display', 'flex');
        $('.capsRow').fadeOut(0);
        $('.hidroRow').fadeOut(0);
        $('.btn3 .whiteLine').removeClass('activeLine');
        $('.btn2 .whiteLine').removeClass('activeLine');
        $('.btn1 .whiteLine').addClass('activeLine');
        $('.btn1').css({"background":"#5c3d6b","color":"#fff"});
        $('.btn2').css({"background":"#ff2c7b","color":"#fff"});
        $('.btn3').css({"background":"#ff2c7b","color":"#fff"}); 
        $('#tabelaNutri').attr('src', require(`@/assets/img/tabelanutri.png`));
        });
        $('#btn2').on('click', function(){
        $('.gummiesRow').fadeOut(0);
        $('.capsRow').css('display', 'flex');
        $('.hidroRow').fadeOut(0);

        $('.btn1 .whiteLine').removeClass('activeLine');
        $('.btn3 .whiteLine').removeClass('activeLine');
        $('.btn2 .whiteLine').addClass('activeLine');

        $('.btn1').css({"background":"#ff2c7b","color":"#fff"});
        $('.btn2').css({"background":"#5c3d6b","color":"#fff"});
        $('.btn3').css({"background":"#ff2c7b","color":"#fff"});             
        });
        $('#btn3').on('click', function(){
        $('.gummiesRow').fadeOut(0);
        $('.capsRow').fadeOut(0);
        $('.hidroRow').css('display', 'flex');
        $('.btn2 .whiteLine').removeClass('activeLine');
        $('.btn1 .whiteLine').removeClass('activeLine');
        $('.btn3 .whiteLine').addClass('activeLine');
        $('.btn1').css({"background":"#ff2c7b","color":"#fff"});
        $('.btn2').css({"background":"#ff2c7b","color":"#fff"});
        $('.btn3').css({"background":"#5c3d6b","color":"#fff"});  
        $('#tabelaNutri').attr('src', require(`@/assets/img/tabelacaps.jpg`));     
        });

           // Troca de bloco no Mobile
        const mediaQuery = window.matchMedia('(max-width:900px)');
        function chamaDiv(){
            if(mediaQuery.matches){
                changeDiv(); 
                changeDiv2(); 
            }
        }
        chamaDiv();
        
        function changeDiv(){
            // var gummies30 = document.querySelector('.gummiesRow #gummies30');
            var gummies90 = document.querySelector('.gummiesRow #gummies90');
            var gummies180 = document.querySelector('.gummiesRow #gummies180');
            var nh30 = document.querySelector('.gummiesRow #nh30');
            var nh90 = document.querySelector('.gummiesRow #nh90');
            var nh180 = document.querySelector('.gummiesRow #nh180');
            var nh12 = document.querySelector('.gummiesRow #nh12');
            var mask = document.querySelector('.gummiesRow #mask');
            var liso = document.querySelector('.gummiesRow #liso');
            var shampoo = document.querySelector('.gummiesRow #shampoo');
                function switchBlock($el, $el1, $el2, $el3, $el4, $el5, $el6, $el7){
                    // if(window.matchMedia('(max-width:768px)')){
                        $el.before($el1);
                        $el2.before($el3);
                        $el4.before($el5);
                        $el6.before($el7);
                        gummies90.style.margin = '70px 0px 25px 0px';
                        shampoo.style.margin = '0px 0px 25px 0px';
                    // }
                }
                switchBlock(gummies180,gummies90, nh90, nh30, nh12, nh180, mask, liso); 
        }
        function changeDiv2(){
            var gummies30 = document.querySelector('.capsRow #gummies30');
            var gummies90 = document.querySelector('.capsRow #gummies90');
            var gummies180 = document.querySelector('.capsRow #gummies180');
            // var nh30 = document.querySelector('.capsRow #nh30');
            var nh90 = document.querySelector('.capsRow #nh90');
            var nh180 = document.querySelector('.capsRow #nh180');
            var nh12 = document.querySelector('.capsRow #nh12');
            var mask = document.querySelector('.capsRow #mask');
            var liso = document.querySelector('.capsRow #liso');
            var shampoo = document.querySelector('.capsRow #shampoo');
                function switchBlock($el, $el1, $el2, $el3, $el4, $el5, $el6, $el7){
                    // if(window.matchMedia('(max-width:768px)')){
                        $el.before($el1);   
                        $el2.before($el3);   
                        $el4.before($el5);   
                        $el6.before($el7);   
                        shampoo.style.margin = '0px 0px 25px 0px';
                        nh90.style.margin = '70px 0px 25px 0px';
                    // }
                }
                switchBlock(nh180,nh90, gummies30, nh12, gummies180, gummies90, mask, liso); 
        }
    },
     data(){ 
        return {
        boxCompraCarrinho: {
        tipo: "produto",
        itens: [
        {
            idProduto: "44",
            idAtributoSimples: "0",
            idUnidadeVenda: "0",
            idArmazem: "0",
            quantidade: "1",
            adicional: "",
            parametros: ""
        }
        ]
        },
        boxCompraCarrinho1: {
        tipo: "produto",
        itens: [
        {
            idProduto: "45",
            idAtributoSimples: "0",
            idUnidadeVenda: "0",
            idArmazem: "0",
            quantidade: "1",
            adicional: "",
            parametros: ""
        },
        ]
        },
        boxCompraCarrinho2: {
        tipo: "produto",
        itens: [
        {
        idProduto: "46",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
        boxCompraCarrinho3: {
        tipo: "produto",
        itens: [
        {
        idProduto: "28",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
        boxCompraCarrinho4: {
        tipo: "produto",
        itens: [
        {
        idProduto: "29",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
        boxCompraCarrinho5: {
        tipo: "produto",
        itens: [
        {
        idProduto: "30",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
        boxCompraCarrinho6: {
        tipo: "produto",
        itens: [
        {
        idProduto: "37",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
        boxCompraCarrinho7: {
        tipo: "produto",
        itens: [
        {
        idProduto: "32",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
        boxCompraCarrinho8: {
        tipo: "produto",
        itens: [
        {
        idProduto: "31",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
        boxCompraCarrinho9: {
        tipo: "produto",
        itens: [
        {
        idProduto: "33",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
    }
    },
    components:{

    },
    methods: {
    addCartBoxCompra() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra1() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho1;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho1.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra2() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho2;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho2.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra3() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho3;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho3.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra4() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho4;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho4.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra5() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho5;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho5.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra6() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho6;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho6.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra7() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho7;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho7.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra8() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho8;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho8.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra9() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho9;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho9.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    }
}
</script>

<style lang="scss" scoped>
.capsRow, .hidroRow{
    display:none;
}

.descontoBox.capBox{
    background-color:#42c7a1 !important;
}
.escolhas .col-12{
    background-color:#ff2c7b;
    border-radius:10px;
}
.produtosBox{
    .titleSection{
        padding:20px 0px;
        h1{
            color:#404040;
            font-family: 'Poppins',sans-serif;
            font-size:40px;
            font-weight: 900;
        }
        p{
            font-weight: 300;
            color:#666666;
            margin-top:-10px;
            font-family: 'Roboto',sans-serif;
        }
    }
    .trocaProduto{
        margin:20px 0px 50px 0px;
        .col-sm-4{
            text-align:center;
            padding:0px 6px;
            cursor:pointer;
            p{
                color:#fff;
                font-family:'Poppins',sans-serif;
                font-weight: 900;
                font-size:30px;
            }
            .whiteLine{
                transition: 0.5s ease;
            }
            .whiteLine.activeLine{
                height:2px;
                background-color:#fff;
                display: block;
                width:25%;
                margin:0 auto;
                position: relative;
                top:-7px;
            }
        }
        .produtoAtivo{
            border-radius:10px;
            transition:0.4s ease;
            background-color:#5c3d6b;
        }
        .produtoInativo{
            transition:0.4s ease;
            border-radius:10px;
            background-color:#ff2c7b;
        }
    }
    p{
        margin:0;
    }
    font-family: 'Roboto',sans-serif !important;
    .btnCompra{
        transition:0.5s ease;
        width:240px;
        height:60px;
        background-color:#04b900;
        color:#fff;
        font-family:'Helvetica',sans-serif;
        font-weight: bold;
        border:none;
        border-radius: 5px;
        margin:10px 0px;
    }
    .btnCompra:hover{
        opacity: 0.7;
    }
    .colCentral{
        border: 1px solid #dadada;
        padding: 0;
        margin:25px 0px;
        .titleBox{
            text-align: center;
            padding:13px 0px;
            background-color:#f2f2f2;
            font-family: 'Roboto',sans-serif;
            p{
                margin:0;
            }
            p:first-child{
                font-weight: bold;
                color:#404040;
                font-size:14px; 
                font-family: 'Roboto',sans
            }
            p:last-child{
                font-weight: normal;
                color:#666666;
                margin-top:-10px;
            }
        }
        .imgBox{
            text-align:center;
            img{
                margin:20px 0px;
                max-height: 200px;
            }
        }
        .descontoBox{
            text-align: center;
            padding:20px 20px;
            background-color:#ff2c7b;
            color:#fff;
            p{
                font-family: 'Roboto',sans-serif;
                font-weight: bold;
            }
        }
        .productForm{
            text-align:right;
            padding-right: 20px;
            s{
                font-size:14px !important;
                font-weight:400;
            }
            p:first-child{
                font-weight: 900;
                color:#000;
                margin:25px 0px 20px 0px;
                font-size:12px;
                line-height:15px;
            }
             span:nth-of-type(1){
                font-weight:600;
                font-size:16px;
            }
            p:nth-of-type(2){
                color:#000;
                font-weight: normal;
            }
            span.price{
                color:#000;
                font-size:50px;
                font-weight: 900;
            }
        }
    }
    
}
@media screen and (max-width:800px){
    .btnCompra{
        width:160px !important;
        height:40px !important;
    }
    span.price{
        font-size:35px !important;
    }
    .descontoBox{
        padding:10px 0px !important;
        p{
            font-size:14px;   
        }
    }
    .titleBox{
        padding:4px !important;
        p:first-child{
            font-size:11px !important;
        }
        p:last-child{
            font-size:10px !important;
            margin-top:2px !important;
        }
    }
    .imgBox{
        img{
            max-width: 90% !important;
        }
    }
    .productForm p{
        font-size:9px !important;
    }
    .colCentral .productForm{
        padding-right:7px !important;
    }
    .flag{
        width: 70% !important;
        position: absolute;
        top: 18% !important;
        left: 0px;
        padding: 5px 0px !important;
        p{
            font-size:12px !important;
        }
    }
    .trocaProduto{
        .escolhas{
            p{
                font-size:25px !important;
            }
        }
    }
    .produtosBox{
     .titleSection{
         padding:20px 0px 0px 0px;
          h1{
        font-size:27px;
        }
        p{
            font-size:12px;
            margin-top:-5px;
        }
     }
     .trocaProduto{
         margin:20px 0px 0px 0px !important;
     }
    }
}
</style>