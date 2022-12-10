<script setup>
import { ref } from "vue";
import { useScroll } from "@vueuse/core";

const scrollBox = ref(null);
const scroll = useScroll(scrollBox);
</script>

<template>
  <div>
    <p class="scroll-box" ref="scrollBox">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab, quo!
      Doloremque quo iure sed ipsa quisquam sit nihil, quibusdam blanditiis
      error. Sequi voluptatem adipisci voluptates unde dignissimos delectus
      reprehenderit, iste suscipit consequatur tempora obcaecati ullam.
      Voluptatibus, tempore! Amet autem consequuntur commodi assumenda, error
      quasi earum. Saepe, quia earum. Aut sunt inventore facere, ducimus laborum
      excepturi neque nihil, illo repellat quo esse animi quibusdam, consectetur
      deleniti eius? Fugit voluptatibus qui placeat nulla architecto. A aperiam
      quisquam aut nisi error eligendi voluptatem nam aliquid minus nemo impedit
      totam, voluptates dolor officia. Facere debitis ipsam, quia, facilis cum
      soluta voluptates unde ullam numquam, natus odit molestias non placeat?
      Autem atque voluptatum eum dolorem! Magni aliquid dolorem aperiam, nulla
      dignissimos laborum? Accusamus quo esse temporibus harum tempora alias
      quibusdam! Neque error, vitae earum cupiditate necessitatibus eius
      veritatis dolore quidem expedita odit temporibus dicta illum aliquid, iste
      eaque, rerum iusto dolorem ad incidunt soluta et omnis? Sit veritatis
      provident, minus laborum voluptas enim voluptatibus voluptatum odio quod
      maxime. Autem nam sapiente dolorum et alias nihil, quia quo fugit amet?
      Fugiat facilis voluptas repellat, assumenda rerum quasi ea possimus
      accusamus culpa aperiam voluptates labore quam consequuntur facere placeat
      animi excepturi exercitationem sunt debitis qui ipsam iure modi. Veniam
      quidem blanditiis enim similique deserunt, doloremque nostrum neque
      explicabo, deleniti doloribus totam nulla natus magni suscipit nam autem
      commodi inventore dicta odio. Harum, veniam aliquid possimus ad dolor
      recusandae, at natus ipsa officia repellat debitis laborum eaque id ullam
      sit mollitia explicabo assumenda dolorem ratione autem. Recusandae culpa,
      voluptates molestiae nisi in commodi dicta expedita! Ea a possimus
      voluptatem quasi, recusandae doloremque incidunt nihil dolorum atque
      labore est, magni nisi aut amet praesentium. Similique saepe totam soluta
      accusamus!
    </p>

    <pre>{{ scroll }}</pre>
  </div>
</template>

<style scoped>
.scroll-box {
  width: 300px;
  height: 300px;
  overflow: auto;
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
