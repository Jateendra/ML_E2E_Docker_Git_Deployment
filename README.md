# ML_E2E_Docker_Git_Deployment

## Problem Statement :

This project is for Boston House pricing prediction using Linear Regression and it's end to end execution using : EDA , model building , docker , Git and Deployment to Heroku cloud .

## Software & Tools requirements :

1 . [Github](https://github.com/)

2 . [Heroku](https://heroku.com)

3 . [VSCode](https://code.visualstudio.com/)

4 . [GitClient](https://git-scm.com/downloads)

## Github , VS Code : Setup and Configuration

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

## Webapp Development by Flask API :


* Create files required for Flask API Webapp Development , such as :

```bash
app.py
templates/home.html
```

* Run app.py : It will generate below URL

```bash
127.0.0.1:5000/
```

* Check it's working on not

## Execution of the Code via Post man :


[Postman_download_link](https://www.postman.com/downloads/)


* Open postman : APIs -> POST -> 127.0.0.1:5000/predict_api

	* Body -> raw -> JSON
        ```bash
        {
            "data":{
            "CRIM":0.00632,
            "ZN":18.0,
            "INDUS":2.31,
            "CHAS":0.0,
            "NOX":0.538,
            "RM":6.575,
            "AGE":65.2,
            "DIS":4.0900,
            "RAD":1.0,
            "TAX":296,
            "PTRATIO":15.3,
            "B":396.90,
            "LSTAT":4.98
            }
        }
        ```

* If you click on Send , you shall get the result like below :
	
	```bash
    30.086495760985294
    ```