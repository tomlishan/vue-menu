<template>
  <div>
    <b-button v-b-toggle.sidebar-backdrop>Toggle Sidebar</b-button>

    <b-sidebar
      id="sidebar-backdrop"
      title="Sidebar with backdrop"
      :backdrop-variant="variant"
      backdrop
      shadow
      bg-variant="dark"
    >
      <div class="px-3 py-2">
        <b-form-group label="Backdrop variant" label-for="backdrop-variant">
          
          
          <b-button variant="primary" block>button A</b-button>
          <b-button variant="primary" block>button B</b-button>
        </b-form-group>
        
      </div>

    <template #footer>
       <div class="d-flex bg-dark text-light align-items-center px-3 py-2">
        <strong class="mr-auto">FooterA</strong>
       </div>
        <div class="d-flex bg-dark text-light align-items-center px-3 py-2">
        <strong class="mr-auto">FooterB</strong>
       </div>
      </template>

    </b-sidebar>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        variant: 'dark',
        
      }
    }
  }
</script>
