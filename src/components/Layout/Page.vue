<template>
  <b-container
    class="
      p-0
      m-0
      overflow-hidden
      d-flex
      flex-column
      justify-content-center
      align-items-center
      bg-white
    "
    :style="pageStyle"
  >
    <b-row class="bg-theme m-0 w-100" :style="{ height: '1.5rem' }" />
    <b-row class="m-0 pt-4 px-5 pb-4 w-100 d-flex flex-grow-1">
      <b-col cols="4" class="m-0 p-0 pr-4 h-100 overflow-hidden">
        <BasicInfo />
        <Section
          v-for="section in resume.basicInfoSections"
          :key="section.title"
          :title="section.title"
          :sectionItems="section.sectionItems"
        />
      </b-col>
      <b-col cols="8" class="m-0 p-0 pl-4 h-100 overflow-hidden">
        <Section
          v-for="section in resume.mainContentSections"
          :key="section.title"
          :title="section.title"
          :sectionItems="section.sectionItems"
        />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
const RESOLUTION = 80; // ppi
const PAGE_WIDTH = 8.5;
const PAGE_HEIGHT = 11;

import BasicInfo from "./BasicInfo";
import Section from "../Section/Section";
import resume from "../../resumes/fall2021.json";

export default {
  name: "Page",
  components: {
    BasicInfo,
    Section,
  },
  data: () => {
    return {
      pageStyle: {
        width: RESOLUTION * PAGE_WIDTH + "px",
        height: RESOLUTION * PAGE_HEIGHT + "px",
      },
      resume: resume,
      contentHeight: "calc(100% - 1.5rem)",
    };
  },
};
</script>