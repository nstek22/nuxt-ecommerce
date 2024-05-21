<template>
    <div class="c-app">
      <div class="c-sidebar c-sidebar-dark c-sidebar-fixed c-sidebar-lg-show" id="sidebar">
        <div class="c-sidebar-brand d-lg-down-none">
          <img src="/images/ns.png" class="bg-light rounded shadow-sm p-2" width="55"> <span class="ml-2 font-weight-bold">NIZAM STORE</span>
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
          <Nuxt />
          <!-- end content -->
  
          <footer class="c-footer">
            <div><strong>nizamstore.com</strong> &copy; 2024 - PT. Nizam Solusi Teknologi.</div>
            <div class="ml-auto">version :&nbsp;1.0-beta</div>
          </footer>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  
    import Header from '@/components/admin/header.vue'
    import Sidebar from '@/components/admin/sidebar.vue'
  
    export default {
  
      //middleware
      middleware: 'isAdmin',
  
      //register components
      components: {
        Header,
        Sidebar
      }
  
    }
  </script>
  
  <style>
  </style>