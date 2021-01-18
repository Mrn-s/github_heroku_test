<template>
  <div id="background_page_medecins">
    <article class="colonne_centrale_a container-fluid">
      <div class="row titre_row">
        <div class="col-sm-12 titre taille_4">
          <p>Retrouvez les réponses à vos questionnaires</p>
        </div>
      </div>
      <div class="row laaa">
        <div class="col-sm-6 la " v-for="re in all_repsonses" v-if="(re.id_patient == user_patient.id)">
          <div class="container res">
            <div class="row">
                <div class="col-sm-12 taille_3 entete" v-for="p in p_bdd" v-if="p.id == re.id_patient">
                    <p>M. {{p.nom}}</p>
                    <p>Questionnaire nº {{re.id_questionnaire}}</p>
                    <p>Identifiant questionnaire : {{ re.id}}</p>
                </div>
            </div>
            <div class="row" v-for="p in p_bdd" v-if="(p.id == re.id_patient) ">
              <div class="col-sm-12 ques" v-for="questio in questionnaires" v-if="questio.id == re.id_questionnaire">
                <div class="col-sm-12 chaque_qq">
                  <p class="taille_2 bold  col-sm-12"> question 1 : {{questio.questions[0].qu}} </p>
                  <p class="taille_1  col-sm-12">votre réponse : 1 < <b class="ma_rep">{{re.reponses.split(',')[1]}}</b> < 4 </p>
                </div>
                <div class="col-sm-12 chaque_qq">
                  <p class="taille_2  col-sm-12 bold"> question 2 : {{questio.questions[1].qu}} </p>
                  <p class="taille_1 col-sm-12">votre réponse : 1 < <b class="ma_rep">{{re.reponses.split(',')[3]}}</b> < 4</p>
                </div>
                <div class="col-sm-12 chaque_qq">
                  <p class="taille_2  col-sm-12 bold"> question 3 : {{questio.questions[2].qu}} </p>
                  <p class="taille_1  col-sm-12">votre réponse : 1 < <b class="ma_rep">{{re.reponses.split(',')[5]}}</b> < 4</p>
                </div>
                <div class="col-sm-12 chaque_qq">
                  <p class="taille_2  col-sm-12 bold">question 4 : {{questio.questions[3].qu}}</p>
                  <p class="taille_1  col-sm-12">votre réponse : 1 < <b class="ma_rep">{{re.reponses.split(',')[7]}}</b> < 4</p>
                </div>
                <div class="col-sm-12 chaque_qq">
                  <p class="taille_2  col-sm-12 bold">question 5 : {{questio.questions[4].qu}}</p>
                  <p class="taille_1  col-sm-12">votre réponse : 1 < <b class="ma_rep">{{re.reponses.split(',')[9]}}</b> < 4</p>
                </div>
                <div class="col-sm-12 chaque_qq">
                  <p class="taille_2  col-sm-12 bold">question 6 : {{questio.questions[5].qu}} </p>
                  <p class="taille_1  col-sm-12">votre réponse : 1 < <b class="ma_rep">{{re.reponses.split(',')[11]}}</b> < 4</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </article>
  </div>
</template>

<script>
  module.exports = {
    props: {
      user_patient: { type: Object },
      p_bdd : { type: Array, default: [] },
      questionnaires: { type: Array, default: [] },
      all_repsonses: { type: Array, default: [] }
    }
  }
</script>

<style scoped>
  .ques{
    max-height: 600px;
    overflow-y: scroll;
  }

  .entete{
    padding-top: 30px ;
    color:white;
  }

  .res{
    border: 2px black solid;
    background-color: var(--bleu_logo_o);
  }

  .chaque_qq{
    background-color: var(--beige_fonce);
    margin: 40px 0;
    padding: 10px;
    color:black;
  }

  .ma_rep{
    background-color: var(--bleu_logo_o);
    color: white;
    font-size: 1.4em;
    padding: 0 4px;
  }

  .titre{
    text-align: center;
  }

  .titre_row{
    background-color: var(--beige_fonce);
    margin-bottom: 30px;
  }

  .laaa{
    background-color: var(--beige_fonce);
  }

  .colonne_centrale_a{
    padding: 0 250px;
  }

  .la{
    margin: 20px 0;
  }

  .chaque_re{
    padding: 30px;
    border: 3px solid black;
  }

  #background_page_medecins{
    background-color: var(--bleu_logo);
    height: 100%;
    max-height: 1660px;
    padding-top: 40px;
    padding-bottom: 190px;
    overflow-y: scroll;
  }

</style>
