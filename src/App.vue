<script setup>
import MyHeader from "@/components/MyHeader.vue";
import MyList from "@/components/MyList.vue";
import SkillsBar from "@/components/SkillsBar.vue";

const formation = [
  {
    firstDate: "2020",
    secondDate: "2022",
    firstValue: "formations.1.formation",
    secondValue: "formations.1.school",
    thirdValue: "formations.1.location",
    fourthValue: "formations.1.hint",
  },
  {
    firstDate: "2019",
    secondDate: "2020",
    firstValue: "formations.2.formation",
    secondValue: "formations.2.school",
    thirdValue: "formations.2.location",
    fourthValue: "formations.2.hint",
  },
  {
    firstDate: "2017",
    secondDate: "2018",
    firstValue: "formations.3.formation",
    secondValue: "formations.3.school",
    thirdValue: "formations.3.location",
    fourthValue: "",
  },
  {
    firstDate: "2015",
    secondDate: "2017",
    firstValue: "formations.4.formation",
    secondValue: "formations.4.school",
    thirdValue: "formations.4.location",
    fourthValue: "",
  },
  {
    firstDate: "2013",
    secondDate: "2015",
    firstValue: "formations.5.formation",
    secondValue: "formations.5.school",
    thirdValue: "formations.5.location",
    fourthValue: "",
  },
];
const experience = [
  {
    firstDate: "2019",
    secondDate: "2022",
    firstValue: "experiences.1.job",
    secondValue: "experiences.1.company",
    thirdValue: "experiences.1.location",
    fourthValue: "experiences.1.hint",
  },
  {
    firstDate: "août 2019",
    secondDate: "sept 2019",
    firstValue: "experiences.2.job",
    secondValue: "experiences.2.company",
    thirdValue: "experiences.2.location",
    fourthValue: "experiences.2.hint",
  },
  {
    firstDate: "2017",
    secondDate: "2018",
    firstValue: "experiences.3.job",
    secondValue: "experiences.3.company",
    thirdValue: "experiences.3.location",
    fourthValue: "experiences.3.hint",
  },
  {
    firstDate: "2013",
    secondDate: "2015",
    firstValue: "experiences.4.job",
    secondValue: "experiences.4.company",
    thirdValue: "experiences.4.location",
    fourthValue: "experiences.4.hint",
  },
  {
    firstDate: "2010",
    secondDate: "2013",
    firstValue: "experiences.5.job",
    secondValue: "experiences.5.company",
    thirdValue: "experiences.5.location",
    fourthValue: "experiences.5.hint",
  },
];
const skills = [
  {
    skillName: "skills.1.skill_name",
    skillValue: 76,
  },
  {
    skillName: "skills.2.skill_name",
    skillValue: 70,
  },
  {
    skillName: "skills.3.skill_name",
    skillValue: 62,
  },
  {
    skillName: "skills.4.skill_name",
    skillValue: 95,
  },
  {
    skillName: "skills.5.skill_name",
    skillValue: 57,
  },
  {
    skillName: "skills.6.skill_name",
    skillValue: 74,
  },
  {
    skillName: "skills.7.skill_name",
    skillValue: 47,
  },
  {
    skillName: "skills.8.skill_name",
    skillValue: 31,
  },
  {
    skillName: "skills.9.skill_name",
    skillValue: 63,
  },
  {
    skillName: "skills.10.skill_name",
    skillValue: 56,
  },
  {
    skillName: "skills.11.skill_name",
    skillValue: 78,
  },
  {
    skillName: "skills.12.skill_name",
    skillValue: 300,
    fourthValue: "it's over 9000!",
  },
];
</script>

<template>
  <MyHeader />
  <div class="flex justify-around mt-6">
    <MyList :datas="formation" title="diploma_title" />
    <MyList :datas="experience" title="work_title" />
  </div>
  <div class="mx-16 mb-10">
    <SkillsBar :datas="skills" title="skills_title" />
  </div>
</template>

<style></style>
