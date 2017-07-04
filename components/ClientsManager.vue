<template>
  <div>
    <p class="field">
      <a class="button is-primary" @click="openModal()">Add new client</a>
    </p>
    <modal-card :class="{'is-active': showNew}" title="New Client" @ok="saveClient()" @close="closeModal()">
      <vz-input type="text" placeholder="Username" v-model="newClient.name"></vz-input>
      <vz-input type="email" placeholder="Email" v-model="newClient.email"></vz-input>
      <vz-input type="password" placeholder="Password" v-model="newClient.password"></vz-input>
    </modal-card>
    <table class="table">
      <thead>
        <tr>
          <th>Username</th>
          <th>Email</th>
          <th>Password</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="client in clients">
          <td>{{ client.name }}</td>
          <td>{{ client.email }}</td>
          <td>{{ client.password }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import ModalCard from '~components/ModalCard'
import VzInput from '~components/VzInput'
export default {
  name: 'clients-manager',
  components: { ModalCard, VzInput },
  data () {
    return {
      showNew: false,
      newClient: {
        name: '',
        email: '',
        password: ''
      },
      clients: []
    }
  },
  methods: {
    openModal () {
      this.showNew = true
    },
    closeModal () {
      this.showNew = false
    },
    saveClient () {
      this.clients.push(this.newClient)
      this.newClient = {
        name: '',
        email: '',
        password: ''
      }
      this.closeModal()
    }
  }
}

</script>

<style>

</style>
