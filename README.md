# RenGine
reNgine is an automated reconnaissance framework for web applications with a focus on highly configurable streamlined recon process via Engines, recon data correlation and organization, continuous monitoring, backed by a database, and simple yet intuitive User Interface. reNgine makes it easy for penetration testers to gather reconnaissance with

Clone this Repo:

    git clone https://github.com/yogeshojha/rengine 

Edit the dotenv file, please make sure to change the password for postgresql POSTGRES_PASSWORD!

     nano .env


In the dotenv file, you may also modify the Scaling Configurations    


      MAX_CONCURRENCY=80
      MIN_CONCURRENCY=10

MAX_CONCURRENCY: This parameter specifies the maximum number of reNgine's concurrent Celery worker processes that can be spawned. In this case, it's set to 80, meaning that the application can utilize up to 80 concurrent worker processes to execute tasks concurrently. This is useful for handling a high volume of scans or when you want to scale up processing power during periods of high demand. If you have more CPU cores, you will need to increase this for maximised performance.

MIN_CONCURRENCY: On the other hand, MIN_CONCURRENCY specifies the minimum number of concurrent worker processes that should be maintained, even during periods of lower demand. In this example, it's set to 10, which means that even when there are fewer tasks to process, at least 10 worker processes will be kept running. This helps ensure that the application can respond promptly to incoming tasks without the overhead of repeatedly starting and stopping worker processes.

These settings allow for dynamic scaling of Celery workers, ensuring that the application efficiently manages its workload by adjusting the number of concurrent workers based on the workload's size and complexity


Run the installation script, Please keep an eye for any prompt, you will also be asked for username and password for reNgine.

     sudo ./install.sh

If install.sh does not have install permission, please change it, chmod +x install.sh

reNgine can now be accessed from https://127.0.0.1 or if you're on the VPS https://your_vps_ip_address

Unless you are on development branch, please do not access reNgine via any ports


      
    
