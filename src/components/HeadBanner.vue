
<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col-sm-12">
                    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
                        <ol class="carousel-indicators">
                            <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
                            <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
                            <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
                        </ol>
                        <div class="carousel-inner">
                            <div class="carousel-item active">
                                <img class="d-block w-100" src="https://imagenesgamers.canalrcn.com/ImgTodoGamers/pokemon_amarillo_retro_portada.jpg" alt="First slide" height="300px" width="1200px">
                                <div class="carousel-caption d-none d-md-block">
                                </div>
                            </div>
                            <div class="carousel-item">
                                <img class="d-block w-100" src="https://i.imgur.com/bWgKnk5.jpg" alt="Second slide" height="300px" width="1200px">
                            </div>
                            <div class="carousel-item">
                                <img class="d-block w-100" src="https://co.godaddy.com/blog/wp-content/uploads/10-c%C3%B3digos-html-para-p%C3%A1ginas-web-y-para-qu%C3%A9-sirven_2.jpg" alt="Third slide" height="300px" width="1200px">
                            </div>
                        </div>
                        <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
                            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                            <span class="sr-only">Previous</span>
                        </a>
                        <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
                            <span class="carousel-control-next-icon" aria-hidden="true"></span>
                            <span class="sr-only">Next</span>
                        </a>
                    </div>
                                        <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark ">
                        <a class="navbar-brand " href="# ">
                            <img src="https://github.com/GaleanoJorge/WorkShop1/blob/master/workshop.png?raw=true" width="166 " height="50" class="d-inline-block align-top " alt="WORKSHOP">
                        </a>
                        <div class="collapse navbar-collapse justify-content-end " id="navbarNav ">
                            <ul class="navbar-nav ">
                                <li class="nav-item active ">
                                    <a class="nav-link " href="# ">Inicio <span class="sr-only">(current)</span></a>
                                </li>
                                <li class="nav-item ">
                                    <a class="nav-link " href="# ">Servicios</a>
                                </li>
                                <li class="nav-item ">
                                    <a class="nav-link " href="# ">Noticias</a>
                                </li>
                                <li class="nav-item ">
                                    <a class="nav-link " href="# ">Equipo</a>
                                </li>
                            </ul>
                        </div>
                    </nav>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
  name: "HeadBanner",
  props: ["banner"],
};
</script>

<style scoped>
</style>

