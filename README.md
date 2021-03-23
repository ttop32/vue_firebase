# vue_firebase
-presonal environment setup note for vue and vuetify with firebase hosting  
--https://ttop324test.web.app/  

# Result
![result](doc/result1.jpg)

# Environment setup

```javascript
//initialise  
npm install -g @vue/cli  
vue create projectname              //set default  
cd projectname  
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
    //select firebase project       its project name
    //public directory              dist  
    //just enter for remain  
npm run build  
    //before run, add below on vue.config.js  
        //module.exports = {  
        //  ... ,  
        //  publicPath: process.env.NODE_ENV === 'production'  ? './' : '/'   
        //}  
firebase deploy --only hosting:sitename  
    //before run, 
        //create sitename from https://console.firebase.google.com/  
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
- [vue](https://vuejs.org/)  
- [firebase](https://vuetifyjs.com/)  
- [vuetify](https://firebase.google.com/)  

- [vue/firebase 이용해서 홈페이지 만들기](https://kyungsnim.net/137)  
