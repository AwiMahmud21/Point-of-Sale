 <template>
  <div class="c-app">
    <div class="c-sidebar c-sidebar-dark c-sidebar-fixed" :class="{ 'c-sidebar-lg-show': !$page.url.startsWith('/apps/transactions') }" id="sidebar">
      <div class="bg-light c-sidebar-brand d-lg-down-none m-t-5 mb-5">
					     <img src="/images/logoku.png" class="rounded shadow-sm p-1" style="width: 90px;margin: 10px 0 10px 0;">
      </div>

      <!-- user -->
      <div class="c-sidebar-title mb-3 ml-3" style="color:#f6f6f6;font-family: Arial, Helvetica, sans-serif;">
            <i class="fa fa-user-md me-2"></i><span class="" :auth="user">{{ auth.user.name }}</span> 
      </div>

      <!-- sidebar -->
      <Sidebar />
      <!-- end sidebar -->

    </div>
    <div class="c-wrapper c-fixed-components">
      
      <!-- header -->
      <Header />
      <!-- end header -->

      <div class="c-body">

        <!-- content -->
        <slot />
        <!-- end content -->

        <footer class="c-footer">
          <div><strong>SarawiStore.</strong> | @copyright2023 - AwiMahmud</div>
        </footer>
      </div>
    </div>
  </div>
</template>

<script>

  import Header from '../Components/Header.vue'
  import Sidebar from '../Components/Sidebar.vue'

  export default {

    //register components
    components: {
      Header,
      Sidebar
    },

    props: {
      auth: Object
    }
  }
</script>

<!-- <style>
</style> -->