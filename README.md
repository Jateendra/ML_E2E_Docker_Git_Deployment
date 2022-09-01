# ML_E2E_Docker_Git_Deployment

## Problem Statement :

This project is for Boston House pricing prediction using Linear Regression and it's end to end execution using : EDA , model building , cocker , Git and Deployment to Heroku cloud .

## Software & Tools requirements :

1 . [Github](https://github.com/)

2 . [Heroku](https://heroku.com)

3 . [VSCode](https://code.visualstudio.com/)

4 . [GitClient](https://git-scm.com/downloads)

## Steps :

1 . Do the "NL_LinearRegression.ipynb" file to produce the model files .

2 . Create a repository in Github .

3 . Open VSCode and use Gitbash :

* Clone the repository :

    ```bash
	git clone https://github.com/Jateendra/ML_E2E_Docker_Git_Deployment.git
    ```

* Copy  "NL_LinearRegression.ipynb" & model files to the current project folder .
	
* Create the conda environment :

    ```bash
    conda create -n ml_boston python==3.7 -y
    conda activate ml_boston ( source activate ml_boston )
    ```

* Create a file with name : requirements.txt

    * Mention the required packages and libraries .
    * Execute the file

        ```bash
        pip install -r requirements.txt
        ```

4 . Configure your VSCode <-> Github links by following below gitbash commands . This will make sure when you commit your codes or push your codes it will be replicated to your Github account .

* Connection for Github via Name

    ```bash
    git config --global user.name "jateendra.pradhan@gmail.com"
    git config --global user.name "Jateendra Pradhan"
    ```

* Execute the below command anytime to check your link

    ```bash
    git config --global user.name
    ```

5 . Commit Codes to github :

[Learn more on Gitcommands](https://www.atlassian.com/git/tutorials/setting-up-a-repository)

* Push file changes to Github

    ```bash
    git add .
    git commit -m "my first commit"
    git push origin main
    ```

* Always check status

    ```bash
    git status   
    ``` 