<template>
  <div>
    <md-card>
      <md-card-header class="remove-padding">
        <Header />
      </md-card-header>

      <md-card-content>
        <NewTodo placeholderMsg="Add a new todos here" />
        <ListOfTodos todos="this.todos" />
        <XofYItems />
      </md-card-content>

      <div class="image-footer">
        <img
          class="image-footer-logo"
          src="https://www.redhat.com/outfit/b64444a376f6be2a8ee78f111930a2aa/Logo-Red_Hat-Open_Innovation_Labs-A-Standard-RGB.png"
          alt="Open Innovation Labs logo"
        />
      </div>
    </md-card>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import NewTodo from "@/components/NewTodo.vue";
import ListOfTodos from "@/components/ListOfTodos.vue";
import XofYItems from "@/components/XofYItems.vue";
import { mapMutations } from "vuex";

export default {
  name: "Todo",
  components: {
    Header,
    ListOfTodos,
    NewTodo,
    XofYItems
  },
  methods: {
    ...mapMutations(["editTodo", "toggleTodo", "deleteTodo"])
  }
};
</script>

<style lang="scss" scoped>
.remove-padding {
  padding: 0px;
}
.md-card {
  width: 480px;
  margin: 4px;
  display: inline-block;
  vertical-align: top;
}
.image-footer {
  border-top: solid;
  margin-top: 1px;
}
.image-footer-logo {
  padding: 5px 0px 5px 0px;
  height: 55px;
}
</style>
