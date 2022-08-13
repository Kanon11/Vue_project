<template>
  <div>
    <div class="user-name" v-if="activeSubscribedPackages.length">
      <ul>
        <li class="small-user">Active auto renewal package</li>
        <li
          class="big-user-title deactivateButton"
          @click="unsubscribe_package(sbPac.message)"
          v-for="sbPac in activeSubscribedPackages"
          :key="sbPac.title"
        >
          {{ sbPac.title }}
        </li>
      </ul>
    </div>
    <div class="modal-background" id="unsubPackage">
      <div class="modal-content pop-02">
        <span class="close" @click="hideModal('unsubPackage')"></span>
        <h1>{{ unsubscribe_msg }}</h1>
      </div>
    </div>
  </div>
</template>

<script>
import $ from 'jquery'
export default {
  name: "modalView",
  data() {
    return {
      activeSubscribedPackages: [
        {
          title: "5 days gp",
          message: "send sms for deregistration to 162775",
        },
        {
          title: "15 days gp",
          message: "send sms for deregistration to 162775",
        },
      ],
      unsubscribe_msg: "",
    };
  },
  methods: {
    showModal(id) {
      $("#" + id).fadeIn(200);
      $("body").toggleClass("no-scroll");
    },
    hideModal(id) {
      $("#" + id).fadeOut(400);
      $("body").toggleClass("no-scroll");
    },
    unsubscribe_package(message) {
      this.unsubscribe_msg = message;
      this.showModal("unsubPackage");
    },
  },
};
</script>
