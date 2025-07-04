React Wedding Card


Introduction




This is a simple wedding invitation web app built with React.js and a module-based structure.




I created it as a wedding gift for two friends who met through me.




Sample: https://uyu423.github.io/react-wedding-card/





Preparations





$ sudo npm install -g yarn
$ yarn




Start





$ npm start




Build & Deploy (using GitHub Pages)




When you build the project, static files will be generated inside build/*. You can easily host these static files using GitHub Pages or any other static hosting service. For detailed instructions, see here.




For deployment, this project uses the built-in create-react-app deployment features along with gh-pages (already included in package.json).




To serve static files correctly, make sure you update the homepage value in package.json to match your repository URL.







$ npm run build
$ npm run deploy




Edit Contents




Most of the data can be edited inside src/config.js.





config.js (export default Object)




const gallery (array): List of images to display in the gallery.




global (object)




googleMapAPIKey: To use Google Maps, you’ll need a Google Map API Key. Make sure your intended hostname is allowed.






comment (object): Supports both LiveRe and Facebook Comments Plugin. Use the enable flag in each object to toggle the plugins on or off. You can use both, either, or neither.




LiveRe: You’ll need a uid
 issued by LiveRe and the service type (city or premium). The city plan 
is free and LiveRe supports multiple SNS logins and anonymous posting.




Facebook: You’ll need an App ID, 
which you can create in the Facebook Developers Center. Make sure to add
 your hostname in the app settings.






title (string): The title displayed in the header bar of the webpage. English text is recommended as the font is set up for English.




wedding (object): Contains details related to the wedding ceremony.




place (object): Information about the wedding venue.




at (string): Wedding date and time in YYYY-MM-DD HH:mm format. Internally, Moment.js is used to convert this to a human-readable format like January 27, 2018, 12:00 PM.




bridal and groom (object): Information about the bride and groom.




image (image): Path to the profile picture. A square (1:1 ratio) image is recommended.




phone (string): Contact number for calls and SMS.




facebook (string): Facebook profile URL. If set to false, the Facebook icon won’t appear.






image (object): Settings related to images.




header (image): Sets the main image displayed below the header.




gallery (array): Uses the const gallery variable defined above.







HTML & Open Graph




Currently, Open Graph meta tags and HTML content need to be updated manually in public/index.html because dynamic replacement is not implemented yet. Check the file for reference.

