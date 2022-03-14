<script setup>
import MyHeader from "./components/MyHeader.vue";
import MyList from "./components/MyList.vue";

const formation = [
  {
    firstDate: "2020",
    secondDate: "2022",
    firstValue:
      "Master - Architecture logiciel, développeur d'applications bac+5",
    secondValue:
      "Epitech - Le futur de l’informatique. Le meilleur de l’innovation.",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
  {
    firstDate: "2019",
    secondDate: "2020",
    firstValue: "Licence - Responsable de Projet Web et Mobile bac+3",
    secondValue:
      "Epitech - Le futur de l’informatique. Le meilleur de l’innovation.",
    thirdValue: "Nancy, France",
    quaterValue: "Major de promotion 2019 - 2020",
  },
  {
    firstDate: "2017",
    secondDate: "2018",
    firstValue:
      "Licence - Techniques et Technologies Avancées de Maintenance bac+3",
    secondValue: "Université de Lorraine.",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
  {
    firstDate: "2015",
    secondDate: "2017",
    firstValue: "Faculté de Sciences - Physique Chimie",
    secondValue: "Université de Lorraine - FST.",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
  {
    firstDate: "2013",
    secondDate: "2015",
    firstValue: "BTS - Maintenance Industrielle bac+2",
    secondValue: "CFAI Lorraine.",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
];
const experience = [
  {
    firstDate: "2019",
    secondDate: "2022",
    firstValue: "Développeur Web Front-End",
    secondValue: "Digitsole.",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
  {
    firstDate: "août 2019",
    secondDate: "sept 2019",
    firstValue: "Développeur Web Front-End",
    secondValue: "60FPS.",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
  {
    firstDate: "2017",
    secondDate: "2018",
    firstValue: "Responsable de projet maintenance",
    secondValue: "NOVARTIS PHARMA",
    thirdValue: "Huningue, France",
    quaterValue:
      "Responsable de projet de maintenance et d'amélioration dans le secteur pharmaceutique et biotechnologies, production de bio-médicaments (anticorps monoclonaux)",
  },
  {
    firstDate: "",
    secondDate: "",
    firstValue: "Faculté de Sciences - Physique Chimie",
    secondValue: "Université de Lorraine - FST",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
  {
    firstDate: "",
    secondDate: "",
    firstValue: "BTS - Maintenance Industrielle bac+2",
    secondValue: "CFAI Lorraine",
    thirdValue: "Nancy, France",
    quaterValue: "",
  },
];
</script>

<template>
  <MyHeader />
  <div class="flex justify-around my-5">
    <MyList :datas="formation" title="Diplôme et Formations" />
    <MyList :datas="experience" title="Expériences professionnelles" />
  </div>
</template>

<style></style>
