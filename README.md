# vue_firebase
environment setup presonal note for vue and vuetify with firebase hosting  
https://ttop324test.web.app/  

# Result
![result](doc/result1.jpg)

# Environment setup

```javascript
//initialise  
npm install -g @vue/cli  
vue create PROJECTNAME              //set default  
cd PROJECTNAME  
vue add vuetify                     //set default  
    
   
//run local server        
npm run serve		  
   
   
//deploy on firebase hosting  
npm install -g firebase-tools  
firebase login  
    //before run, from https://console.firebase.google.com/  
        //create account
        //create project
firebase init	  	                
    //select features               hosting  
    //select an option              existing project
    //select firebase project       created project from https://console.firebase.google.com
    //public directory              dist  
    //just enter for remain  
npm run build  
    //before run, add below on vue.config.js  
        //module.exports = {  
        //  ... ,  
        //  publicPath: process.env.NODE_ENV === 'production'  ? './' : '/'   
        //}  
firebase deploy --only hosting:SITENAME  
    //before run, 
        //create sitename from https://console.firebase.google.com/  
            //select its projectname  
            //select hosting   
            //click add another site  
            //define SITENAME to your own site name  
        //add below on firebase.json     
            //{  
            //    "hosting": {  
            //        "site": "SITENAME",  
            //        ...  
            //    }   
            //}  

  ```

# Acknowledgement and References
- [vue](https://vuejs.org/)  
- [firebase](https://vuetifyjs.com/)  
- [vuetify](https://firebase.google.com/)  

- [vue/firebase 이용해서 홈페이지 만들기](https://kyungsnim.net/137)  
