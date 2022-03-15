<script setup>
import MyHeader from "@/components/MyHeader.vue";
import MyList from "@/components/MyList.vue";
import SkillsBar from "@/components/SkillsBar.vue";

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
    quaterValue:
      "Développeur web Vue.js, Node.js sur l'application de e-santé Podo Smart. ",
  },
  {
    firstDate: "août 2019",
    secondDate: "sept 2019",
    firstValue: "Développeur Web Front-End",
    secondValue: "60FPS.",
    thirdValue: "Nancy, France",
    quaterValue: "Développeur de site web, emploi d'été.",
  },
  {
    firstDate: "2017",
    secondDate: "2018",
    firstValue: "Responsable de projets maintenance",
    secondValue: "NOVARTIS PHARMA",
    thirdValue: "Huningue, France",
    quaterValue:
      "Responsable de projet de maintenance et d'amélioration dans le secteur pharmaceutique et biotechnologies, production de bio-médicaments (anticorps monoclonaux).",
  },
  {
    firstDate: "2013",
    secondDate: "2015",
    firstValue: "Technicien supérieur de maintenance",
    secondValue: "FIVES CRYO",
    thirdValue: "Golbey, France",
    quaterValue:
      "Technicien supérieur dans le milieu de la conception d'échangeurs thermiques à plaques et ondes en aluminium brasées.",
  },
  {
    firstDate: "2010",
    secondDate: "2013",
    firstValue: "Technicien de maintenance",
    secondValue: "POMPES SERVICE LORRAINE",
    thirdValue: "Nancy, France",
    quaterValue:
      "Technicien de maintenance industriel dans le secteur des pompes centrifuges et volumétriques.",
  },
];
const skills = [
  {
    skillName: "Html Css",
    skillValue: 76,
  },
  {
    skillName: "Linux",
    skillValue: 62,
  },
  {
    skillName: "MacOS",
    skillValue: 95,
  },
  {
    skillName: "Node.js",
    skillValue: 45,
  },
  {
    skillName: "Vue.js",
    skillValue: 74,
  },
  {
    skillName: "Python",
    skillValue: 47,
  },
  {
    skillName: "MongoDB",
    skillValue: 31,
  },
  {
    skillName: "Anglais",
    skillValue: 42,
    quaterValue: "it's over 9000!",
  },
  {
    skillName: "Curiosité",
    skillValue: 900,
    quaterValue: "it's over 9000!",
  },
];
// const hobbies = [{}];
</script>

<template>
  <MyHeader />
  <div class="flex justify-around mt-8">
    <MyList :datas="formation" title="Diplôme et Formations" />
    <MyList :datas="experience" title="Expériences professionnelles" />
  </div>
  <div class="mx-16">
    <SkillsBar :datas="skills" title="Compétances" />
  </div>
</template>

<style></style>
