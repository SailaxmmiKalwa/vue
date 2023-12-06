<template>
    <div class="card">
      <div class="card-image">
        <img 
          src="https://corporate.walmart.com/content/corporate/en_us/about/jcr:content/par/grid_4_copy_copy/parsys_tab_1/image.img.jpg/1693432306522.jpg" 
          alt="Company Logo" v-if="id==0" 
        />
        <img 
          src="https://1000logos.net/wp-content/uploads/2021/10/Saudi-Aramco-logo.png" 
          alt="Company Logo" v-if="id==1" 
        />
        <img 
          src="https://1000logos.net/wp-content/uploads/2021/08/State-Grid-Corporation-of-China-Logo.png" 
          alt="Company Logo" v-if="id==2"
        /> 
        <img 
          src="https://m.media-amazon.com/images/G/01/gc/designs/livepreview/a_generic_white_10_us_noto_email_v2016_us-main._CB627448186_.png" 
          alt="Company Logo" v-if="id==3"
        />
        <img 
          src="https://www.gtreview.com/wp-content/uploads/2015/01/Vitol_logo_bg-768x514.jpg" 
          alt="Company Logo" v-if="id==4"
        />
      </div>
      <div class="card-content">
        <h1 class="company-name">{{ companiesList[id].CompanyName }}</h1>
        <p class="industry"><b>{{ companiesList[id].IndustryType }}</b></p>
        <div class="highlighter">
          <span class="label">Headquarters</span>
          <span class="value"><b>{{ companiesList[id].Headquarters }}</b></span>
        </div>
        <div class="highlighter">
          <span class="label">Employees</span>
          <span class="value">{{ companiesList[id].Employees }}</span>
        </div>
        <div class="highlighter">
          <span class="label">Revenue</span>
          <span class="value">{{ companiesList[id].RevenueInUSD }}</span>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name : 'cardcomponent',
    props : ['id','companiesList']

  };
  </script>
  
  <style scoped>
  .card {
    display: flex;
    flex-direction: column;
    width: 400px;
    border: 2px solid #000000;
    border-radius: 10px;
    overflow: hidden;
    margin: 30px;
    background-color: #fdfdff;
  }
  
  .card-image {
    height: 150px;
    overflow: hidden;
  }
  
  .card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  
  .card-content {
    padding: 16px;
  }
  
  .company-name {
    font-size: 24px;
    margin-bottom: 8px;
  }
  
  .industry {
    font-size: 16px;
    margin-bottom: 16px;
  }
  
  .highlighter {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #f0f0f0;
    padding: 8px;
    border-radius: 4px;
    margin-bottom: 8px;
    border: 0.7px solid black;
    transform: scale(1.05); 
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  .label {
    font-size: 16px;
    font-weight: bold;
    color: #151515;
  }
  
  .value {
    font-size: 13px;
    color: #262626;
  }

  @media screen and (max-width: 600px) {
.card {
    display: flex;
    flex-direction: column;
    width: 300px;
    border: 1px solid #ccc;
    border-radius: 8px;
    overflow: hidden;
    margin: 10px;
  }
  }


  </style>
  