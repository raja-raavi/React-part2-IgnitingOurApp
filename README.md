Day : 2 - Episode : 1
=====================

NPM - package managers

NPM init

Package.json is a configuration for NPM. It keeps the track of whatversion of package is installed in our project

webPack, parcel, wheat all these are bundlers - The job of bundlers is bundler or packages our app propelry into clean, concise and chuncking. so that it can be shipped to production

npm install -D parcel

There are 2 types of packages that we can install

1. Dev Dependencies - It is generally required in a developement phase
2. Normal Dependencies - It can be used in production also

Difference b/w caret(^) and tilday(~) in devDependency:
=======================================================

If any minor update comes tomorrow then caret will automaticlly update to minor update and (it always recommended to use)

TillDay will automaticlly do the major update and (it's not recommended to use)

Package-lock.json - It will keep the exact version of pacakges of all the dependencies. When we deploying our code to PD this package-lock.josn will help us to keep the exact version in PD
Integrity - Working in Dev but not in PD? sha15.. What ever the same on local it should be same on PD

Node_Modules - It's like teh data base of all the packages that our project needs

We Just installed only parcel but why other packages are installed in node_modules - This is because parcel needs some dependencies to work and that other dependencies needs some dependencies to work and viceversa
This is called as Transitive Dependencies

How may package.json files are present in our project - Not one, In the node_modules each package contains it's own package.json file

DAY - 2 : Episode - 2
=====================
 
npx parcel index.html - executing the parcel bundler and setting the index.html is the source
Just like we have npm lly we have npx
 
npm is used to install a packages
npx is used to exceute a package
 
There are 2 ways to get react into our project
 
1. CDN links - It's not a good practice because we are making network/http call here so that it will not good one
2. npm packages - Here we are installing react pages into node modules so it easy to us
 
npm install react - to install react
 
npm install react-dom
 
If you install the above 2 commands but still we get error as "React is not defined" in the console this is beacuse react is installed in node_modules but we haven't used it
to use React we need to import react and reactDOM
 
Yot tought it's enough to start react right - NO, If we fireup recat app then again we got error as "Browser scripts cannot have imports and exports" 
This is beacuse browser thinks that the script tag in index.html as a plain java script file but it's dsn't right? it includes recat we need to tell browser this script tag is a
module type i.e type = "module"
 
#parcel
- DevBuild
- Local Setver
- HMR = Hot Moudle Replacement i.e when we chnage anything in or app it will refresh the page and chnages are applied in webPage 
- File Watching Algorithim - written in C++ = Parcel keeps an eye in all the files thats how it tracks all the changes
- Caching - Faster Builds = It will reduce the build time each and every time when we saving this is done by Caching
- Image Optimization
- Minification our file  = when we do prodution build
- Bundling
- Compressing
- Consistent Hashing
- Code splitting
- Differential Bundling = suppout older browsers
- Diagnostics - Detailed erros
- Error Handling
- HTTPS
- Tree Shaking = when we have 100's of fnis our code but we use only 4 out of them then parcel will tree shake our code (It willremove unused code)
- Different dev and prod bundles
 
How the react app is fast? DO you think because of react is faster? Obviously yes but no - Bundler's makes the app super faster than react.

For prodution build - npx parcel build index.html
we got error at this step because npm set main file as "App.js" in the package.json file so we have to remove mian