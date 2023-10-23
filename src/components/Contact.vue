<template>
    <div class="p-10">
        <div id="contactenos-title-container" class="h-min">
            <i id="icon-mail" class="bi bi-envelope-fill"></i>
            <h1 class="h-min">CONTACTENOS</h1>
        </div>
        <div id="form" class="lg:w-2/3 max-w-[700px] mx-auto sm:p-10">
            <form action="https://formsubmit.co/9cf75f9a1c2350bc0a0086a40e299f77" method="POST">
                <div class="grid grid-cols-1 mb-6">
                    <input type="text" name="name" placeholder="nombre" required>
                    <input type="email" name="email" placeholder="email" required>
                    <input type="tel" name="telefono" placeholder="telefono">
                </div>
                <textarea placeholder="deje un comentario" name="message" id="" cols="40" rows="10" class="w-full h-[200px]"></textarea>
                <div class="text-center">
                <input id="submit-button" type="submit" value="Enviar">
                </div>
            </form>
        </div>
    </div>
</template>

<style scoped>
input {
    background-color: rgba(0, 0, 0, 0.05);
    border: 2px solid #eaedf2;
    color: rgb(70, 69, 69);
    padding-left: 10px;
    margin-top: 15px;
}

textarea {
    background-color: rgba(0, 0, 0, 0.05);
    border: 2px solid #eaedf2;
    padding-left: 10px;
    padding-right: 10px;
}
::placeholder {
  color: rgb(70, 69, 69);
  opacity: 1;
  font-size: 18px;
}

input:focus, textarea:focus  {
    outline: solid 2px #969696;
}
#icon-mail {
    position: relative;
    display: block;
    left: 50%;
    top: -43px;
    margin-left: -50px;
    color: #F6BC07;
    background-color: white;
    font-size: 33px;
    line-height: 50px;
    width: 100px;
    height: 50px;
}
#contactenos-title-container {
    text-align: center;
    border-top: 2px solid #eaedf2;
    border-bottom: none;
    padding-bottom: 0;
    padding-top: 16px;
    margin: 90px 0 0 0;
}
h1 {
    position: relative;
    top: -50px;
    text-transform: uppercase;
    font-weight: 700;
    margin: 20px 0 0 0;
    font-size: 26px;
}
#submit-button {
    cursor: pointer;
    padding: 10px 80px 10px 80px;
    margin-bottom: 30px;
    margin-top: 10px;
    margin-left: 15px;
    background-color: #F6BC07;
    border-color: #F6BC07;
    background-image: none;
    color: white;
}
</style>