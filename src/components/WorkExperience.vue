<template>
  <section>
    <h2 class="title">
      My<br /><strong class="strong-title-item">Work Experience</strong>
    </h2>
    <div class="center">
      <ul>
        <WorkDescription
          v-for="(description, index) in workDescriptions"
          :key="index"
          :position="description.position"
          :context="description.context"
          :description="description.description"
        />
      </ul>
    </div>
  </section>
</template>

<script setup>
import WorkDescription from "./WorkDescription.vue";
const workDescriptions = [
  {
    position: "Art teacher",
    context: "HELHa, Leuze-en-Hainaut, Sep 2023 - Jun 2024",
    description:
      "Taught visual arts to future primary school teachers and future secondary school teachers of French, aiming to develop their artistic and creative skills.",
  },
  {
    position: "Web Designer (intern)",
    context: "Aerospacelab, Mont-Saint-Guibert, Jun 2023 - Aug 2023",
    description:
      "Redesigned the user interface of an existing application using Figma, including creating wireframes, prototypes, and a design system. Integrated the design into Nuxt.js with Tailwind CSS.",
  },
  {
    position: "Production Manager",
    context: "Dargaud-Lombard, Brussels, Jul 2019 - Nov 2021",
    description:
      "Directed reprint and co-publishing projects, ensuring deadlines and budgets were met. Managed the reprints of comic books by planning and coordinating stock needs and distributor requests. Coordinated the production of co-published books with Standaard Uitgeverij and performed quality control of comic books, handling any potential disputes.",
  },
  {
    position: "Prepress Designer",
    context: "Dargaud-Lombard, Brussels, Jul 2010 - Jul 2019",
    description:
      "Coordinated comic production processes. Used Adobe Suite for layout and image editing. Prepared files for printing, adhering to technical standards and strict deadlines. Communicated with internal and external stakeholders.",
  },
];
</script>

<style scoped>
ul {
  all: unset;
  color: var(--secondary);
  font-family: "Open Sans", sans-serif;
  display: flex;
  flex-direction: column;
  max-width: 44rem;
}

.center {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
