<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="light">
      <b-navbar-brand href="#"><img src="/img/logomaqvermelha.png" width="150px"/></b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">
            <i class="fas fa-location-arrow mr-1 "></i>
            <span>Rotinas</span>
          </b-nav-item>
          <b-nav-item href="#">
            <i class="fas fa-briefcase mr-1 "></i>
            <span>Tarefas</span>
          </b-nav-item>
          <b-nav-item href="#">
            <i class="fas fa-pen-square mr-1 "></i>
            <span>Bloco de Notas</span>
          </b-nav-item>
          <b-nav-item href="#">
            <i class="fas fa-table mr-1 "></i>
            <span>Brainstorm</span>
          </b-nav-item>
          <b-nav-item href="#">
            <i class="fas fa-tachometer-alt mr-1 "></i>
            <span>Dashboard</span>
          </b-nav-item>
        </b-navbar-nav>

        

        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown no-caret  class="demo-navbar-user" >
            <template slot="button-content">
              <span class="d-inline-flex flex-lg-row-reverse align-items-center align-middle">
                <span
                 
                >Workspace: Maq-Larem</span>
              </span>
            </template>

            <b-dd-item>
              Workspace: 
            </b-dd-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown no-caret  class="demo-navbar-user" >
            <template slot="button-content">
              <i class="fas fa-bell"></i>
            </template>
            <b-dd-item>
              Workspace: 
            </b-dd-item>
          </b-nav-item-dropdown>

          <b-nav-item  class="demo-navbar-user" >
            <i class="fas fa-comments"></i>
          </b-nav-item>


          <div
          class="nav-item mt-2 mx-2 d-lg-block text-big font-weight-light line-height-1 opacity-25"
          >|</div>


          <b-nav-item-dropdown text="Aluisio" right class="demo-navbar-user">
            <template slot="button-content" class="menu">
              <span class="d-inline-flex flex-lg-row-reverse align-items-center align-middle">
                <span
                  class="" style="width:140px"
                >Aluisio</span>
              </span>
            </template>


            <b-dropdown-item href="#"> 
              <i class="fas fa-user-circle mr-1"></i>
              <span>Meu perfil</span>
            </b-dropdown-item>
            <b-dd-divider/>
            <b-dropdown-item href="#">
              <i class="fas fa-clock mr-1 danger"></i>
              <span class="danger">Cadastro de Rotinas</span>
            </b-dropdown-item>
            <b-dropdown-item href="#">
              <i class="fas fa-cog mr-1"></i>
              <span>Configurações</span>
            </b-dropdown-item>
            <b-dropdown-item href="#">
              <i class="fas fa-users mr-1"></i>
              <span>Usuários</span>
            </b-dropdown-item>
            <b-dropdown-item href="#">
              <i class="fas fa-chart-pie mr-1"></i>
              <span>Workspaces</span>
            </b-dropdown-item>
            <b-dd-divider />
            <b-dropdown-item target="_blank" href="/manuais/manual-do-usuario.pdf">
              <i class="fas fa-book-open mr-1"></i>
              <span>Manual</span>
            </b-dropdown-item>
            <b-dd-divider />
            
            <b-dropdown-item href="#" >
              <i class="fas fa-sign-out-alt mr-1"></i>
              <span>Sair</span>
            </b-dropdown-item>
          </b-nav-item-dropdown>

        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>


<style scoped lang="css">
.grey{
    /* text-color:rgb(177, 177, 177); */
    font-size: 14px;
}

.black{
    /* text-color: rgb(73, 73, 73); */
    font-size: 14px;
}

.danger{
    /* text-color: #840F0F; */
    font-size: 14px;
}

</style>

<script>
// import { router } from '../../routers/router'
// import { eraseCookie } from "../../utils/utils"


export default {
  name: 'NavBar',
  methods: {
    // logout (){
    //   // eraseCookie("access")
    //   // eraseCookie("refresh")
    //   // router.push('/login')
    // }
  }
}
</script>