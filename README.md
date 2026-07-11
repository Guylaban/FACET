<div align="center">
    <h1>FACET</h1>
    <h3>Facial-Affect Conversational Experimentation Testbed</h3>
    <p>An open, privacy-preserving <b>experimentation platform</b> for real-time, <b>affect-adaptive</b> conversations with Large Language Models. FACET extends <a href="https://doi.org/10.1145/3687272.3688296">Lexi</a> with an on-device facial valence&ndash;arousal loop, so any text agent can adapt to a user's facial affect without any image leaving the machine.</p>
</div>

## 🌍 Project Overview

This platform is designed to facilitate advanced research in the field of user-bot interactions and LLMS models. It offers a comprehensive environment for conducting, monitoring, and analyzing experiments in this cutting-edge domain.

## 🚀 Quick Start

To set up and start using the project, follow these steps:

### Step 0: Download the following pre-requirements:

Node.JS - <a href="https://nodejs.org/en">https://nodejs.org/en</a><br>
Npm - <a href="https://docs.npmjs.com/downloading-and-installing-node-js-and-npm">https://docs.npmjs.com/downloading-and-installing-node-js-and-npm</a><br>
Git - <a href ="https://git-scm.com/downloads">https://git-scm.com/downloads</a><br>
Python 3 - <a href ="https://www.python.org/downloads/">https://www.python.org/downloads/<br>
OpenAI api key - <a href ="https://help.openai.com/en/articles/4936850-where-do-i-find-my-api-key">OpenAI api key info</a>

### Step 1: Set Up MongoDB Database

Before setting up the project, you'll need a MongoDB database. You can set this up locally on your machine, or use MongoDB Atlas for a cloud-based solution.

- **Setting up MongoDB Locally:**
  Follow [this guide](https://docs.mongodb.com/manual/installation/) to install MongoDB locally on your system.

- **Setting up MongoDB on Atlas:**
  MongoDB Atlas offers a cloud-based solution. You can set up a free cluster following [this guide](https://docs.atlas.mongodb.com/getting-started/).

  **Make sure you are adding your ip to be white listed**

### Step 2: Clone the Repository

```bash
git clone https://github.com/Guylaban/FACET.git
```

### Step 3: Install Dependencies

- For the client:
  ```bash
  cd client
  npm run setup
  ```

- For the server:
  ```bash
  cd server
  npm run setup
  ```

### Setup Process Details

During the setup process, you'll be guided through a series of prompts to configure your environment:

- `OPENAI_API_KEY`: Enter your OpenAI API key.
- `MONGODB_USER`: Enter the MongoDB username.
- `MONGODB_PASSWORD`: Enter the password for MongoDB.
- `MONGODB_URL`: Provide the MongoDB URL (mongodb+srv://<cluster-name>.mongodb.net).
- `MONGODB_DB_NAME`: Choose a name for your MongoDB database.

Additionally, the setup script will guide you in creating an administrative user for your system. You'll need to provide a username and password for this user.

### Functions of the Setup Script

The setup script automates several important tasks to get your server up and running:

- **Configures Environment Variables**: 
  - It creates a `.env` file containing essential environment variables like your OpenAI API key, MongoDB credentials, and other necessary configurations.
- **Installs Dependencies**: 
  - Executes `npm install` to install all the necessary npm packages that the server requires to function properly.
- **Builds the Project**: 
  - Runs the build process for your TypeScript code, compiling it and preparing your server for execution.
- **Initializes Admin User**: 
  - Creates an admin user within your system using the credentials you provide, facilitating immediate access to admin-level features.

This comprehensive setup ensures that all necessary components are correctly configured, laying the foundation for a smooth and efficient operation of the server.

### Step 4: Install pip requirements

Run the following command inside the FACET folder from terminal.
```bash
pip install -r requirements.txt
```

Further make sure to install FaceChannel with:
```bash
pip install FaceChannel
```
In addition, add the h5 files from the models folder of this repository into the:
```bash
C:\Users\<USERNAME>\.conda\envs\lexi\lib\site-packages\FaceChannel\FaceChannelV1\TrainedNetworks
```
Or similar folder of your python environment.

### Step 5: Running the Project

- For the Client:
    ```bash
    cd client
    npm start
    ```

**client will run on: http://localhost:3000**

- For the Server:
    ```bash
    cd server
    npm run dev
    ``` 
**server will run on: http://localhost:5000**

- For action unit extaction:
  ```bash
  python AU_extractor.py
  ```

Encountering difficulties with your local environment setup? Consult our [Troubleshooting Guide](TROUBLESHOOTING.md) for assistance in resolving your issues.

## 🌐 Deployment

Intersted to deploy Lexi? Please read our [Deployment Guide](DEPLOYMENT.md) for information on how to deploy.

## 🛠️ Contributing

Interested in contributing? We value your input and contributions! Please read our [Contributing Guidelines](CONTRIBUTION.md) for information on how to get started.

## 🔗 Useful Links

- [Project Homepage](https://www.lexi.network/project-overview)
- [Research Paper](#) (Link to related research papers or articles)

## 📄 License

This project is licensed under the [CC BY-NC 4.0 License](LICENSE.md).

## 📞 Contact

For any inquiries or further information, reach out to us at [laban@bgu.ac.il](mailto:laban@bgu.ac.il).

## 👍 Show Your Support

Give a ⭐️ if this project helped you! Your support encourages us tremendously.

## 📄 Citation

If you use FACET, please cite the accompanying system-demonstration paper (manuscript under review) and the original Lexi platform:

```bibtex
@misc{facet2026,
  title  = {An Open, Privacy-Preserving Experimentation Platform for Real-Time Affect-Adaptive Conversational Studies with Large Language Models},
  author = {Mehra, Vaibhav and Laban, Guy and Gunes, Hatice},
  year   = {2026},
  note   = {Manuscript under review}
}
```

## 📝 License

Released under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See [LICENSE](LICENSE).
