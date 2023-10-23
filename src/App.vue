<template>
  <div>
    <div class="container">
      <div class="innercontainer">
        <div class="content__body">
          <div class="actioncontainer">
            <button class="usedAppsbutton" :class="{ active: filter === 'Installed' }"  @click="showInstalledApps">
              <i class="fa-solid fa-bolt-lightning"></i>Your Apps
            </button>
            <button class="availableapps__btn" :class="{ active: filter === 'Download' }" @click="showDownloadedApps">
              <i class="fa-brands fa-adn"></i> Apps Available
            </button>
          </div>
          <div class="apps__display">
            <div class="appsdisplay__container">
              <div class="search">
                <input type="search" name="search" placeholder="search for an app" />
              </div>
              <div class="allaplic">
                <h3>{{ title }} (  {{ filter === 'Installed' ? installedAppsCount : availableAppsCount }} )</h3>
                <div class="allapliccontainer">
                  <span
                    _ngcontent-tpy-c49=""
                    class="landing-apps"
                    v-for="item in filteredItems"
                    :key="item"
                    :class="{ shimmer: isLoading }"
                  >
                    <a _ngcontent-tpy-c49="" data-track="select application">
                      <span _ngcontent-tpy-c49="" :class="{ activated: filter === 'Installed' }" class="new-features">{{ item.status }}</span>
                     
                      <div _ngcontent-tpy-c49="" class="service-icon-logo">
                        <img class="smallimg" _ngcontent-tpy-c49="" :src="item.logo" alt="Vend" />
                      </div>
                      <p _ngcontent-tpy-c49="">{{ item.apptitle }}</p>
                    </a>
                   
                  </span>
                </div>
                <div class="loadmore">
                  <button class="loadmore__btn">Load More</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "UsersApplication",
  data() {
    return {
      items: [
        {
          apptitle: 'Vend',
          logo: 'https://pipedream.com/s.v0/app_mWnhAp/logo/48',
          status: 'Download'
        },
        {
          apptitle: 'Airtable',
          logo: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYI0SdC_3xBMmEvh43Dao1SI9Y_n7qqFeSbQ&usqp=CAU',
          status: 'installed'
        },
        {
          apptitle: 'shippo',
          logo: 'https://assets-global.website-files.com/6462967bbf70fa5b5b227351/646bd3ac70ee08fca9869afe_shippo-logo-dark.svg',
          status: 'Download'
        },
        {
          apptitle: 'Loyverse',
          logo: 'https://loyverse.com/sites/all/themes/loyversecom/logo.svg',
          status: 'installed'
        },
        {
          apptitle: 'storyChief',
          logo: 'https://assets-global.website-files.com/62d66b587db794f6131223e0/62d679136a81955d33635572_logo.svg',
          status: 'download'
        },
        {
          apptitle: 'Kanban Tools',
          logo: 'https://is1-ssl.mzstatic.com/image/thumb/Purple116/v4/03/2a/24/032a241c-50ad-8fde-bfa4-cd5031e85b23/AppIcon-0-0-1x_U007emarketing-0-0-0-10-0-0-sRGB-0-0-0-GLES2_U002c0-512MB-85-220-0-0.png/1200x630wa.png',
          status: 'installed'
        },
        {
          apptitle: 'Netlify',
          logo: 'https://cdn.sanity.io/images/o0o2tn5x/production/b7112574694a0fd30064faaa252ad555777cb439-1200x676.png?',
          status: 'download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'installed'
        },
        {
          apptitle: 'Mailchimp',
          logo: 'https://assets.stickpng.com/thumbs/58417f77a6515b1e0ad75a2c.png',
          status: 'Download'
        },
        {
          apptitle: 'Etsy',
          logo: 'https://1000logos.net/wp-content/uploads/2017/12/Etsy-emblem.jpg',
          status: 'installed'
        },
        {
          apptitle: 'Basin',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Aweber',
          logo: 'https://www.simplesat.io/wp-content/uploads/2021/12/aweber.png',
          status: 'installed'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Amazon SQS',
          logo: 'https://miro.medium.com/v2/resize:fit:360/1*qoA4HkaQTAAWHb_tMTi0UA.png',
          status: 'Download'
        },
        {
          apptitle: 'Basecamp',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        }
      ],
      filter: "Download",
      title: "All Applications",
       isLoading: true,
    };
  },
  computed: {
    filteredItems() {
      if (this.filter === "Download") {
        return this.items.filter(item => item.status.toLowerCase() === "download");
      } if (this.filter === "Installed") {
        return this.items.filter(item => item.status.toLowerCase() === "installed");
      } else  {
        return this.items;
      }
    },
    installedAppsCount() {
      return this.items.filter(item => item.status.toLowerCase() === "installed").length;
    },
    availableAppsCount() {
      return this.items.filter(item => item.status.toLowerCase() === "download").length;
    }
  },
  methods: {
    showDownloadedApps() {
      this.filter = "Download";
      this.title ="Download More Apps";
      setTimeout(() => {
      this.isLoading = false;
    }, 2000);
    },
    showInstalledApps() {
      this.filter = "Installed";
      this.title = "Installed App";
     
      this.isLoading = false;
   
    }
  },
   mounted() {
    
    setTimeout(() => {
      this.isLoading = false;
    }, 2000);
  },
};
</script>

<style scoped>
.container {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.innercontainer {
  width: 80%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  /* background: orange; */
}

.content__body {
  width: 75%;
  /*  background: green; */
  /* box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px; */
}

.actioncontainer {
  width: 100%;
  display: flex;
  flex-flow: row wrap;
  margin: 0.5rem 0;
  padding-bottom: 0;
  padding-top: 0;
  align-items: center;
  justify-content: flex-start;
  gap: 2rem;
}

.usedAppsbutton,.availableapps__btn {
  border: 2px solid hsla(0, 0%, 50%, 0.8);
  box-shadow: 0 7px 30px -10px rgb(150 170 180/50%);
  width: 200px;
  background-color: #f6f9ff;
  background-color: #fff;
  transform: translateY(0);
  -webkit-transform: translateY(0);
  transition: all 0.4s ease-in-out;
  -webkit-transition: all 0.4s ease-in-out;
  z-index: 1;
  align-self: stretch;
  position: relative;
  min-height: 55px;
  border-radius: 0.5rem;
  cursor:pointer;
}


.active  {
  border: 2px solid #0077f4;
  box-shadow: 0 7px 30px -10px rgb(150 170 180/50%);
  width: 200px;
  background-color: #f6f9ff;
  color: #2e2f31;
  transform: translateY(0);
  -webkit-transform: translateY(0);
  transition: all 0.4s ease-in-out;
  -webkit-transition: all 0.4s ease-in-out;
  z-index: 1;
  align-self: stretch;
  position: relative;
  min-height: 55px;
  border-radius: 0.5rem;
  font-size: 16px;
  font-weight: 600;
}


/* .media-items {
    display: grid;
    grid-template-columns: 50px 1fr 40px;
    padding: 0;
    width: 230px;
    min-height: 50px;
    border: 1px solid #ccc;
    border-radius: 10px;
    max-width: 100%;
   
} */

.apps__display {
  width: 100%;
  margin-top: 26px;
  padding: 20px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  border-radius: 0.5rem;
}

.appsdisplay__container {
  width: 100%;
}

.search {
  width: 100%;
  margin-bottom: 15px;
}

.search input {
  width: 100%;
  padding: 8px;
  border-radius: 0.5rem;
  border: 2px solid #0077f4;
}

.allaplic {
  width: 100%;
}

.allaplic h3 {
  font-family: 'open sans Helvetica sans-serif';
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 22px;
  color: #000;
  margin-bottom: 24px;
}

.service-icon-logo {
  width: 15px;
  height: 15px;
  flex: 0 0 35px;
  box-shadow: 0 7px 30px -10px rgba(150, 170, 180, 0.5);
  background-color: #fff;
  border-radius: 5px;
  padding: 0.5rem;
  margin-right: 10px;
  display: flex;
  border: 1px solid rgba(0, 0, 0, 0.1);
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.service-icon-logo img {
  max-width: 100%;
  height: auto;
}

.landing-apps {
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 100%;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 0.75rem;
  width: 252px;
  min-height: 104px;
  background-color: #fff;
  transform: translateY(0);
  -webkit-transform: translateY(0);
  transition: all 0.4s ease-in-out;
  -webkit-transition: all 0.4s ease-in-out;
}

.landing-apps:hover {
  border: 1px solid #0077f4;
  cursor: pointer;
}

.landing-apps a {
  padding: 1rem 0.7rem 0.7rem;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  color: #000;
  font-weight: 600;
  width: 100%;
  cursor: pointer;
  text-decoration: none;
  list-style-type: none;
  font-size: 17px;
  line-height: 19px;
  font-style: normal;
}
.new-features {
  position: absolute;
  right: 0;
  top: 0;
  font-size: 14px;
  background-color: #00c3ff;
  color: #fff;
  border-radius: 0 0.75rem;
  width: 80px;
  text-align: center;
  font-weight: 700;
  padding: 1px;
}

.activated {
  background-color: black;
}

.smallimg {
  width: 80%;
  height: 50%;
}

.loadmore {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
}

.loadmore__btn {
  color: #fff;
  font-weight: 600;
  position: relative;
  background-color: #000000;
  border-radius: 25px;
  text-align: center;
  padding: 10px 30px;
  width: 200px;
  font-size: 14px;
  border: none;
  cursor: pointer;
}

.loadmore__btn:hover {
  background-color: #464343;
}

.allapliccontainer {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-wrap: wrap;
  gap: 8px 20px;
}


.shimmer::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(to right, #f6f7f8 8%, #eaebed 18%, #f6f7f8 33%);
  background-size: 800px 104px;
  animation: shimmer 1s infinite linear;
}

</style>