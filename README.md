# vue_firebase
use vue and vuetify with firebase hosting
https://ttop324test.web.app/

# Result


# Environment setup

```
//initisalise  
npm install -g @vue/cli  
vue create projectname              //set default  
cd projectname  
vue add vuetify		                //set default  
  
//run local server        
npm run serve		  

//deploy on firebase hosting  
npm install -g firebase-tools  
firebase login  
firebase init	  	                
    //feature= hosting  
    //existing project, select its project name,  
        //create project from https://console.firebase.google.com/  
    //public directory= dist  
    //just enter for remain  
npm run build  
    //add below on vue.config.js  
        //module.exports = {  
        //  ... ,  
        //  publicPath: process.env.NODE_ENV === 'production'  ? './' : '/'   
        //}  
firebase deploy --only hosting:sitename  
    //create sitename     
        //https://console.firebase.google.com/  
        //select its projectname  
        //select hosting   
        //add another site  
        //define sitename  
    //add below on firebase.json     
        //{  
        //    "hosting": {  
        //        "site": "sitename",  
        //        ...  
        //    }   
        //}  
          
  ```

# Acknowledgement and References
- [vue/firebase 이용해서 홈페이지 만들기](https://kyungsnim.net/137)  
