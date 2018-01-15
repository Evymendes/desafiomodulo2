<template>
  <div>
    <div class="menu">
      <img class="menuHamburguer" src="../assets/menu hamburguer.svg">
      <img class="menuLogo" src="../assets/logo.svg">
      <img class="menuLupa" src="../assets/Lupa-busca.svg">
    </div>
    <div class="corpo">
      <h2 class="corpoTitulo"> De tanto ganhar meias de Natal, tio-avô ganha livro e tanta calçá-lo</h2>
      <img class="corpoImagem" src="../assets/cacarlivros.jpg">
      <p class="corpoTexto"> Foi uma cena estranha no Natal antecipado da família Siqueira, na Zona Norte do Rio de Janeiro. Bem mais estranha do que a tia Julinha perguntando à sobrinha Cássia pela 76° vez quando ela ia se casar. Ou o cunhado Valcir tentando entoar Então é Natal, da Simone. Eram quase onze da noite quando o tio-avô Onofre, de 77 anos, ganhou seu presente. Abriu e era um livro, a biografia de Jô Soares, que sua irmã Olga comprara com ótimo preço na Saraiva. Onofre olhou, olhou e olhou o livro por muitos minutos. Os parentes imaginaram que ele estava emocionado. De repente Onofre se sentou, tirou seu sapato e colocou o livro perto do pé. A família demorou a entender: ele estava tentando calçar o livro. resultado das meias que ganhou nos últimos 17 anos.</p>
    </div>
    <div class="rodape">
      <div class="rodapeComentario">
      <ul>
        <li>
          Comentários
        </li>
      </ul>
      </div>
      <div class="rodapeRespostas">
        <img class="rodapeRespostasImagem" src="../assets/profile.svg"> 
         <label>
          <input v-model="comentario" v-on:keyup.enter="addComentario">
          <button v-on:click="comentario()" v-on:keyup.enter="addComentario">Enviar</button>
        </label>  
        <ul class="feito" v-for="rotina in usuario.descricao">
          <li>
            {{rotina}}
          </li>
        </ul>     
      </div>
      <div class="rodapeComentarioUm">
        <img class="rodapeComentarioUmImagem" src="../assets/profile2.svg">
        <div class="testandoUm">
        <p class="rodapeComentarioUmNome"> Camila RJ</p>
        <p class="rodapeComentarioUmRecado">"Eu teria feito o mesmo sinceramente. Papai Noel nunca me deu oq pedi"</p>
        </div>
      </div>
      <div class="rodapeComentarioDois">
        <img class="rodapeComentarioDoisImagem" src="../assets/profile3.svg">
        <div class="testando">
        <p class="rodapeComentarioDoisNome">Joaquim Campinas</p>
        <p class="rodapeComentarioDoisRecado">"kkkkkkkkkkkkkkkkkkkk rindo até 2049. Muito engraçado!!!!!"</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      comentario: "",
        ComentarioSegundo: "",
        usuario: {
          descricao: []
        }
        }
      },
        methods: {
          addComentario(comentario) {
            return this.usuario.descricao.push(this.comentario),
              this.comentario = ""
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
html{
  margin: 0;
}

body{
  background: black;
  margin: 0;
}
.menu {
  margin: 0;
  background: black;
  display: flex;
  justify-content: space-around;
}

.menuHamburguer{
  width: 62px;
}

.menuLogo{
  width: 311px;
}

.menuLupa{
  width: 48px;
}

.corpoTitulo{
  margin: 40px 24px 20px 24px;
  font-size: 38px;
  color: black;
  text-align: center;
  font-weight: bold;
  line-height: 50px; 
}
.corpoImagem{
  width: 96%;
  margin: 0 16px;
}

.corpoTexto{
  color: black;
  font-size: 28.4px;
  margin: 30px 41px;
  text-align: left;
}

.rodapeComentario ul li{
 
  border-bottom: 2px solid #000;
  font-size: 29px;
  letter-spacing: 1.2px;
  color: black;
  font-weight: bold;
  text-align: left;
  list-style: none;
}

.rodapeRespostasImagem{
  width: 130px;
  margin: 0 46px 0 -204px;
}

.rodapeComentarioUm{
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 11px;
  color: #979797;
  margin: 0 0 0 -62px;
}

.rodapeComentarioUmImagem{
  width: 130px;
  margin: 0 52px 0 0;
}

.testandoUm{

}
.rodapeComentarioUmNome{
  font-size: 23px;
  font-weight: bold;
  color: #000000;
  text-align: left;
}

.rodapeComentarioUmRecado{
  font-size: 23px;
    width: 369px;
    text-align: left;
    color: #979797;
}

.rodapeComentarioDois{
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 11px;
    color: #979797;
    margin: 0 0 0 -62px;
}

.rodapeComentarioDoisImagem{
  width: 130px;
  margin: 0 52px 0 0;
}
 

.rodapeComentarioDoisNome{
  font-size: 23px;
  font-weight: bold;
  color: #000000;
  text-align: left;
}

.rodapeComentarioDoisRecado{
    font-size: 23px;
    width: 369px;
    text-align: left;
    color: #979797;
}

.inicio {
  text-align: center;
}

.header {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.header-feito {
  width: 33.33%;
}

.feito li{
  list-style: none;
}

</style>