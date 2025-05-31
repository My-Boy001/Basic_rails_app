# **Hello Rails App**

A basic Ruby on Rails application to demonstrate setup and development using Rails on **WSL (Windows Subsystem for Linux)**.

## **🧰 Requirements**

* **WSL** (Ubuntu recommended)  
* **Ruby** (e.g., 3.0.0+)  
* **Rails** (e.g., 7.x)  
* **Node.js** and **Yarn**  
* **Bundler**  
* **SQLite3** or **PostgreSQL**

## **⚙️ WSL Setup Steps**

### **1\. Install WSL (if not already installed)**

Open PowerShell as Administrator and run:

wsl \--install

Install Ubuntu when prompted, then restart.

### **2\. Install Ruby, Rails & Dependencies inside WSL**

Once inside Ubuntu (WSL terminal):

\# Update package list  
sudo apt update && sudo apt upgrade \-y

\# Install dependencies  
sudo apt install curl git nodejs yarn sqlite3 libsqlite3-dev build-essential libssl-dev libreadline-dev zlib1g-dev \-y

\# Install Ruby using rbenv (recommended)  
curl \-fsSL https://github.com/rbenv/rbenv-installer/raw/main/bin/rbenv-installer | bash

\# Add rbenv to bash  
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' \>\> \~/.bashrc  
echo 'eval "$(rbenv init \- bash)"' \>\> \~/.bashrc  
source \~/.bashrc

\# Install Ruby  
rbenv install 3.2.2  
rbenv global 3.2.2

\# Install Rails  
gem install rails

## **🚀 Project Setup**

### **1\. Clone the Repository**

git clone https://github.com/My-Boy001/Basic\_rails\_app.git  
cd Basic\_rails\_app

### **2\. Install Dependencies**

bundle install

### **3\. Setup Database**

bin/rails db:setup

### **4\. Start the Rails Server**

bin/rails server

Now, open your browser and visit: http://localhost:3000  
If you're running from WSL, use localhost on your Windows browser directly.

## **⬆️ Pushing to GitHub**

Once you've made changes to your project and want to save them to GitHub, follow these steps:

1. **Add your changes:**  
   git add .

   This command stages all your changes for the next commit.  
2. **Commit your changes:**  
   git commit \-m "Your descriptive commit message here"

   Replace "Your descriptive commit message here" with a short, clear message about what you changed.  
3. **Push to GitHub:**  
   git push origin main

   This sends your committed changes to the main branch of your repository on GitHub. If your main branch is named master, use git push origin master instead.

## **🧪 Run Tests**

If tests are available:

bin/rails test  
\# or if using RSpec  
bundle exec rspec

