Symfosys
--------

Symfosys is a DevOps library for Symfony2 applications. It integrates Chef, Vagrant, and 
Capifony. Simply clone the repo, configure with your project and version, run `bundle` 
followed `vagrant up` and watch things go.

The project is in its infancy, and contributors are welcome. Check the Road Map to see 
where the plan is headed. https://github.com/Eponymi/Symfosys/tree/master/doc/roadmap.md

Requirements
------------
  - Vagrant http://www.vagrantup.com
  - Rubygems
  - `bundler` gem
  - **TO-DO:** automate installation of dependencies; add Boxen support. 

Installation
------------
  **Github**
  `git clone https://github.com/Eponymi/Symfosys.git`
  **Composer**
  TO-DO
  **Rubygem**
  TO-DO
  
Usage
-----
  **Install Symfosys and its requirements** (see above).
  
  **Configure**
  1. Configure package settings in `roles/app.json` (defaults to 
  symfony/framework-standard-edition and 2.2.x-dev respectively).
    
    ```json
    {
    ...
      "symfony2": {
        "composer": {
          "package_name": "sylius/sylius",
          "package_version": "*"
        }
      }
    }
    ```
    
   2. Configure project variables like the IP of your Virtual Machine (see `Projectvars`)
   
   **Install required gems**
   `$ bundle`
   
   **Launch your dev machine**
   `$ vagrant up dev`
