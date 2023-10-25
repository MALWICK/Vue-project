<template>
  <div>
    <input type="text" v-model="input" />
    <br />
    <!-- {{ filteredItems }} -->
    <ul v-for="item in filteredItems" :key="item.id">
      <li>{{ item.apptitle }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: '',
      debouncedInput: '',
      items: [
      {id:1,
      apptitle: 'Vend',
      logo: 'https://pipedream.com/s.v0/app_mWnhAp/logo/48',
      status: 'Download'
    },
    {id:2,
      apptitle: 'Airtable',
      logo: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYI0SdC_3xBMmEvh43Dao1SI9Y_n7qqFeSbQ&usqp=CAU',
      status: 'installed'
    },
    {
      id:3,
      apptitle: 'shippo',
      logo: 'https://assets-global.website-files.com/6462967bbf70fa5b5b227351/646bd3ac70ee08fca9869afe_shippo-logo-dark.svg',
      status: 'Download'
    },
    {
      id:4,
      apptitle: 'Loyverse',
      logo: 'https://loyverse.com/sites/all/themes/loyversecom/logo.svg',
      status: 'installed'
    },
    {
      id:5,
      apptitle: 'storyChief',
      logo: 'https://assets-global.website-files.com/62d66b587db794f6131223e0/62d679136a81955d33635572_logo.svg',
      status: 'download'
    },
    {
      id:6,
      apptitle: 'Kanban Tools',
      logo: 'https://is1-ssl.mzstatic.com/image/thumb/Purple116/v4/03/2a/24/032a241c-50ad-8fde-bfa4-cd5031e85b23/AppIcon-0-0-1x_U007emarketing-0-0-0-10-0-0-sRGB-0-0-0-GLES2_U002c0-512MB-85-220-0-0.png/1200x630wa.png',
      status: 'installed'
    },
      ],
      timeout: null
    }
  },
  computed: {
    filteredItems() {
      if (!this.debouncedInput) {
        return this.items; // Return all items if no search query
      }

      const query = this.debouncedInput.toLowerCase();
      return this.items.filter(item => item.apptitle.toLowerCase().includes(query));
    }
  },
  watch: {
    input() {
      clearTimeout(this.timeout);
      this.timeout = setTimeout(() => {
        this.debouncedInput = this.input;
      }, 3000);
    }
  }
};
</script>
