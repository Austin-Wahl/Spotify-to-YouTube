
# Spotify to YouTube playlist conversion tool

Easily convert Spotify songs to Youtube Playlists

  

### Some things to note

- This tool may not be perfect. It works by generating a keyword search with the Spotify song title and artists and taking the first result from YouTube. It may not be 100% accurate.

- You will need to create a Google Developer Console application (a guide is listed below)

- You will need to create a Spotify Developer Application (a guide is listed below)

# Setting up a Google Developer Account

 1. Go to https://console.developers.google.com/ and <b>sign</b> in with the <b>Google account you want the playlist on
 2. Next to the Google Cloud logo, clikc on <b>Select a Project</b>
 3. Click on <b>New project</b>
 4. Give the project a name
 5. Leave organization set as `No organization`
 6. Click **Create**
 7. Wait for the project to finish creating. Then click **Select a project** again and select the project you just created
 8. On the dashboard, the page that says "Welcome" and has "You're working in \<project name here>", click on **APIs and Services**. It's under the Quick access header.
 9. On the left hand side in the navigation bar, find the **Credentials** link and click it.
 10. On the top, you will see a **Create Credentials** link, click it. 
 11. Choose **OAuth client ID**
 12. You'll need to configure the Consent screen. Click on the **Configure Consent Screen** button then the **Get Started** button
 13. Under **App Information** name the app anything. I recommend`Spotify-YouTube converter` for the name and just choose your email for **User support email**
 14. Click **Next** then under **Audience**, choose **External**
 15. Click **Next** then under **Contact Information** just put your email address
 16. Click **Next** then under **Finish** check the **I agree** statement.
 17. Click **Finish**
 18. On the navigation bar on the left side, click **Clients** then click **Create Client**
 19. Set the **Application type** to **Desktop app** and name it. You can leave the name as defaulted.
 20. After you've created the client, click on it.
 21. Under **Aditional information** find **Client secrets**. There will be a section that says **Client secret** with a downward facing arrow. Download the **JSON** file to the root directory of this notebook. **RENAME THE DOWNLOADED FILE TO `creds` BEFORE DOWNLOADING.**
 22. Click on **Audience** in the side menu on the left. Then find **Test users**. Add your email address to it. Because this application is not published and approved by Google, only test users will be able to signin to it. 
 23. Click on the Google Cloud logo and **APIs and Services** again.
 24. Click **Enable APIs and Services** and search for **YouTube Data API v3**
 25. Click on it and click the **Enable** button.
 26. Your done setting up the Google side of things.

# Setting up a Spotify Developer Account
1. Go to https://developer.spotify.com/ and sign in and navigate to your **Dashboard**
2. Click on **Create app**
3. Name the app. Add a description. It does not matter what.
4. For **Redirect URIs** put `http://localhost:3000`. This doesn't matter for this application as its not relying a client web server or anything.
5. Under **Which API/SDKs are you planning to use?** select **Web API**
6. Accept the terms
7. When your redirected to the apps dashboard, click on the **Settings** button on the top.
8. Copy the **Client ID** and paste it into the cell under the variable `SPOTIFY_CLIENT_ID`
9. Copy the **Client SECRET** and paste it into the cell under the variable `SPOTIFY_CLIENT_SECRET`
10. Your done setting up the Spotify side of things. 

# Running the Notebook

 1. Download from the GitHub repo.
 2. Make sure you have a Jupyter environment or download the Jupyter extension in VS code
 3. Make sure python is downloaded on your machine
 4. Open the Notebook in your environment and select the Kernel
 5. I recommend running each cell 1 by 1 but you can click on the Run All button if you prefer.
 6. **You need to have a playlist on YouTube created first before running the Notebook. This application does not create a YouTube playlist.**
7.) Follow the steps as prompted. 

# Bugs
Uh just figure it out. I am not maintaining this. I may make a web app for this at somepoint. I will post it here if I do.
