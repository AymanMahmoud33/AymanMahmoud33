<h1 align="center">Hi 👋, I'm Ayman Aly Mahmoud</h1>
<h3 align="center">Cloud Architect and Trainer</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=aymanmahmoud33&label=Profile%20views&color=0e75b6&style=flat" alt="aymanmahmoud33" /> </p>

- 🔭 I’m currently working on **AWS**

- 👯 I’m looking to collaborate on **Cloud solutions**

- 📝 I regularly write articles on [https://dev.to/aymanmahmoud33](https://dev.to/aymanmahmoud33)

- 💬 Ask me about **AWS, cloud solutions, courses and content creation**

- 📫 How to reach me **se.ayman@gmail.com**

### Blogs posts
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://dev.to/aymanmahmoud33" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/devto.svg" alt="aymanmahmoud33" height="30" width="40" /></a>
<a href="https://linkedin.com/in/https://www.linkedin.com/in/ayman-mahmoud/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/in/ayman-mahmoud/" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://azure.microsoft.com/en-in/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/microsoft_azure/microsoft_azure-icon.svg" alt="azure" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://kubernetes.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

# Blog posts

<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->
Create a folder named .github and create workflows folder inside it if it doesn't exist.
Create a new file named blog-post-workflow.yml with the following contents inside the workflows folder:
name: Latest blog post workflow
on:
  schedule:
    # Runs every hour
    - cron: '0 * * * *'
jobs: 
    update-readme-with-blog: 
        name: Update this repo's README with latest blog posts
        runs-on: ubuntu-latest
        steps: 
            - uses: actions/checkout@v2
            - uses: gautamkrishnar/blog-post-workflow@master
              with: 
                max_post_count: "4"
                feed_list: "https://dev.to/feed/aymanmahmoud33"
