<template>
  <div class="background_page_accueil">
    <div class="c_fluid container-fluid">
      <section class="ligne container-fluid" id ="background_un">
        <article class="row">
          <div class="col-sm-5 partie_gauche_un">
            <div class="container">
              <div class="row">
                <p class="taille_5 bold col-sm-12" id ="titre_un">SANT'EFREI : votre évaluation personnalisé en quelques clics.</p>
                <p class ="taille_3 col-sm-12">Pour tous, partout, à tout moment.</p>
                <p class ="taille_3 col-sm-12"> Inscrivez-vous et trouvez les solutions à vos problèmes de santé !</p>
              </div>
            </div>
            <article class="row" v-if ="!user_medecin.id && !user_patient.id" id = "emplacement_bouton_un_un">
              <router-link id="btn_inscrivez_vous" class="taille_3 btn-13 custom-btn-1-bis col-sm-12" to='/register'>Je m'inscris</router-link>
            </article>
          </div>
          <!-- <div class="col-sm-7">
          </div> -->
        </article>
        <article class="row partie_2">
          <div class="col-sm-5 partie_gauche_deux">
            <div class="container">
              <div class="row">
                <p class="taille_4 bold col-sm-12" id ="titre_deux">Notre histoire</p>
                <p class ="taille_2 col-sm-12">Le besoin d'un site regroupant des outils performants et pertinents mis à dispositions de tous n'a jamais été aussi présent qu'en pleine épidémie mondiale.</p>
                <p class ="taille_2 col-sm-12">C'est dans ce contexte difficile que SANT'EFREI naquit.</p>
              </div>
            </div>
          </div>
          <!-- <div class="col-sm-7">
          </div> -->
        </article>
      </section>

      <section class ="ligne container">
        <article id="deux_un" class="row">
          <p class="taille_5 col-sm-12 bold comment_ca_marche"> Comment ça marche ? </p>
          <p class="taille_2 col-sm-12">
            En quelques clics,
            créez votre compte puis prenez rendez-vous avec votre médecin, choisissez ou non de lui faire part de vos symptômes.<br>

            Trouvez le questionnaire de santé qui vous correspond le plus, repondez-y et trouvez les réponses à vos questions de santé ! <br>
            Ces questionnaires classiques regroupent les problèmes de santé les plus courants et vous permettent d'avoir un aperçu des maladies qui vous touchent. <br>
            Téléchargez le compte rendu, et décidez ou non de le partager avec votre médecin. C'est facile !
          </p>
        </article>
      </section>

      <section class="ligne container-fluid">
        <div class="row">
          <article class="col-sm-5" id="trois_un">
          </article>
          <div class="col-sm-7" id="trois_deux">
            <div class="contenu_trois">
              <div class="row ligne_dans_l3">
                <div class="col-sm-1">
                </div>
                <div class="col-sm-2" id="icone_1">
                </div>
                <div class="col-sm-9">
                  <p class="taille_3 bold col-sm-12">Communiquer</p>
                  <p class="taille_1 col-sm-12 p_l3">Selon vos maux, sélectionnez le type de spécialiste que vous souhaitez consulter et indiquez vos symptômes. Vous pouvez en envoyer jusqu'à 10 directement à votre médecin.</p>
                </div>
              </div>
              <div class="row ligne_dans_l3">
                <div class="col-sm-1">
                </div>
                <div class="col-sm-2" id="icone_2">
                </div>
                <div class="col-sm-9">
                  <p class="taille_3 bold col-sm-12">Proposer un rendez-vous à votre médecin </p>
                  <p class="taille_1 col-sm-12 p_l3">Une fois vos symptômes séléctionnées, vous pouvez les envoyer à votre médecin et lui proposer un créneau de consultation.</p>
                </div>
              </div>
              <div class="row ligne_dans_l3">
                <div class="col-sm-1 ">
                </div>
                <div class="col-sm-2 " id="icone_3">
                </div>
                <div class="col-sm-9">
                  <p class="taille_3 bold col-sm-12">Répondre à une proposition de rendez-vous. </p>
                  <p class="taille_1 col-sm-12 p_l3"> Votre médecin peut vous proposer un rendez-vous et un créneau. Le choix d'accepter ou non vous revient..</p>
                </div>
              </div>
              <div class="row ligne_dans_l3">
                <div class="col-sm-1">
                </div>
                <div class="col-sm-2 " id="icone_4">
                </div>
                <div class="col-sm-9">
                  <p class="taille_3 bold col-sm-12">Se tenir à jour </p>
                  <p class="taille_1 col-sm-12 p_l3"> Ne ratez rien des actualités du monde de la santé et rendez vous sur la rubrique Actualité.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="ligne container">
        <article id="text_quatre" class="taille_5 row bold">
          <p > Un véritable gain de temps, pour le patient et le médecin.</p>
        </article>
      </section>

      <section class="container-fluid" id ="ligne_5">
        <article id="cinq_un" class="container">
          <p class="row taille_5">Témoignages </p>
          <p id ="sous_text_cinq" class="taille_1 row">
             « Ce site m'a permis de prendre contact rapidement avec mon médecin.
             De plus, le temps de consultation est réduit, et l'attente pour avoir un rendez-vous aussi,
             puisque le médecin étudie ma fiche de symptômes avant mon arrivée ! ».
          </p>
          <p class="taille_2" id="noms_temoignages">Adam, 32 ans </p>
        </article>
      </section>
    </div>
  </div>
</template>

<script>

  module.exports = {
    props: {
      user_medecin: { type: Object },
      user_patient: { type: Object }
    },
    data () {
      return {
      }
    },
    methods: {
    }
  }
</script>

<style scoped>
.c_fluid{
  overflow-x: hidden;
}
  .ligne_dans_l3{
    margin: 30px 0;
  }
  #icone_3{
    background-size: contain;
    background-repeat: no-repeat;
    background-image: url("../images/logo_calendrier.png");
  }
  #icone_4{
    background-size: contain;
    background-repeat: no-repeat;
    background-image: url("../images/logo_news.png");
  }
  #icone_1{
    background-size: contain;
    background-repeat: no-repeat;
    background-image: url("../images/logo_com.png");
  }
  #icone_2{
    background-size: contain;
    background-repeat: no-repeat;
    background-image: url("../images/logo_pa.png");
  }

  .comment_ca_marche{
    text-align: center;
  }
  .partie_2{
    margin-top: 80px;
  }

  #titre_un, #titre_deux{
    text-align:center;
  }

  .custom-btn-1-bis {
    padding: 5px 20px;
    font-weight: 500;

    outline: none !important;
    cursor: pointer;
    transition: all 0.4s ease;
    position: relative;

  }
  #btn_inscrivez_vous{
    text-decoration: none;
    color:var(--bleu_logo);
  }

  .partie_gauche_un{
    background-color: var(--beige_fonce_o);
    padding: 25px 30px 10px 60px;
  }
  .partie_gauche_deux{
    background-color: var(--bleu_logo_o);
    color:white;
    padding: 25px 30px 25px 60px;
  }

  .background_page_accueil::-webkit-scrollbar {
      display: none;
  }

  .background_page_accueil{
    background-color: var(--beige);
    height: 100%;
    padding-bottom: 54px;
    overflow-y: scroll;
    /* padding: 0 !important; */
  }

  .contenu_trois{
    margin: 0 5% 0 5%;
  }

  #text_quatre{
    text-align: center;
  }

  .container-fluid{
    background-color: var(--beige);
  }
  .ligne{
    margin-bottom: 4%;
    color: #09371F;
  }

  #background_un{
    background-image: url("../images/background_un.png");
    height: 1200px;
    background-size: cover;
    background-repeat: no-repeat;
    padding-top: 52px;
    width: 100%;
    z-index: 1;
  }

  #emplacement_bouton_un_un{
    padding: 0 30px 0 30px;
    text-align: center;
  }

  #deux_un{
      padding: 10px 25px;
      border: var(--vert_o) 8px double;
      box-shadow: 10px 10px 5px #09371F;;
  }

  #trois_un{
    border-left: 1px black solid;
    border-top: 1px black solid;
    border-bottom: 1px black solid;
    background-size: contain;
    background-repeat: no-repeat;
    background-image: url("../images/background_deux.png");
    background-attachment: fixed;
    height: auto;
  }

  #trois_deux{
    border-left: 1px black solid;
    border-top: 1px black solid;
    border-bottom: 1px black solid;
    border-right: 1px solid black;
    padding: 40px 0;
  }

  .container-fluid{
    padding-right: 0 !important;
    padding-left: 0 !important;
  }

  #ligne_5{
    margin: 0 !important;
    width:100%;
    height: 733px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-size: cover;
    background-repeat: no-repeat;
    background-image: url("../images/background_trois.png");
  }

  #cinq_un{
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px black solid;
    background-color: #FBFBF3;
    width: 40%;
    height: auto;
  }

  #sous_text_cinq{
    width: 60%;
    text-align: center;
  }

  #noms_temoignages{
    padding: 2%;
    background-color: #E8C542;
  }

  .lien {
    transition: 0.3s ease;
    background-color: #FBFBF3;
    color: #09371F;
    text-decoration: none;
    border-top: 4px solid #FBFBF3;
    border-bottom: 4px solid #FBFBF3;
    padding: 20px 0;
    margin: 0 20px;
  }

  .lien:hover {
    border-top: 4px solid #09371F;
    border-bottom: 4px solid #09371F;
    padding: 6px 0;
  }

</style>
