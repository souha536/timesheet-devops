pipeline {
    agent any

    stages {
        stage('Récupérer le code') {
            steps {
                // Récupère le code source depuis le dépôt Git
                git 'https://github.com/souha536/timesheet-devops.git'
            }
        }
        stage('Compiler le projet') {
            steps {
                // Commande Maven pour compiler le projet
                sh 'mvn clean compile'
            }
        }
        stage('Exécuter les tests') {
            steps {
                // Commande Maven pour exécuter les tests
                sh 'mvn test'
            }
        }
        stage('Créer le package') {
            steps {
                // Commande Maven pour créer le package
                sh 'mvn package'
            }
        }
        stage('Déployer l\'application') {
            steps {
                // Commande pour déployer l'application (ajoute ta commande ici)
                echo 'Déploiement de l\'application...'
            }
        }
    }

    post {
        success {
            echo 'Le pipeline s\'est terminé avec succès !'
        }
        failure {
            echo 'Le pipeline a échoué.'
        }
    }
}

