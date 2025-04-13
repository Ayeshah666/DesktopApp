1. Create a new repository on GitHub
2. Open VSCode
3. Create a folder for your application
4. In the same folder, create index.html and index.js files
5. in the terminal use "cd "....your application path"
6. In this folder, write "npm init" command
7. Then write "npm install --save-dev electron" command 
8. A file package.json should have been added. add the following command in the scripts part:  "start": "electron ." after removing the test part.
in the node_module folder create a file name preload.js.

10. Init GitHub in your app folder using "git init" in terminal
11. Connect this folder to your GitHub repository using the "git remote add origin ..." command with your repository URL.
12. Now to avoid pushing a too heavy file to GitHub, we will have to create a new file .gitignore that contains at least this line: node_modules/
(You can see my .gitignore file that contains more elements for git to ignore)
13. To make your folder even less heavy, write "git lfs install" command and write these commands:

git lfs track "*.png"
git lfs track "*.jpg"
git lfs track "*.psd"
git lfs track "*.mp4"
git lfs track "*.exe"

14. Now you can push your app project on Github using the commands:

git add .
git commit -m 'initialization'
git push -u origin master

15. To run your application, write "npm start" in your terminal
16. To make your application a ready-to-use desktop application, write these commands in your terminal:

npm install --save-dev @electron-forge/cli
npm exec --package=@electron-forge/cli -c "electron-forge import"
npm run make


THIS IS IT ! Have fun !
