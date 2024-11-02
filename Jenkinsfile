pipeline {
agent any
triggers {
pollSCM('H/5 * * * *')
}
environment {
DOCKERHUB_CREDENTIALS = credentials ( ’0000’)
IMAGE_NAME_SERVER = ’[ username ]/ mern-server’
IMAGE_NAME_CLIENT = ’[ username ]/ mern-client’
}
stages {
stage ( ’Checkout’) {
steps {
git branch : ’main’ ,
url: 'git@github.com:haninhn/jenkisTp3.git',
credentialsId: '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'
}
}
stage ( ’Build Server Image’) {
steps {
dir ( ’server’) {
script {
dockerImageServer = docker . build (" $ {
IMAGE_NAME_SERVER }")
}
}
}
}
stage ( ’Build Client Image’) {
steps {
dir ( ’ client ’) {
script {
dockerImageClient = docker . build (" $ {
IMAGE_NAME_CLIENT }")
}
}
}
}
stage ( ’Scan Server Image’) {
steps {
script {
sh """
docker run -- rm -v / var / run / docker . sock
:/ var / run / docker . sock \\
aquasec / trivy : latest image -- exit - code 0
-- severity LOW , MEDIUM , HIGH , CRITICAL
\\
$ { IMAGE_NAME_SERVER }
"""
}
}
}
stage ( ’Scan Client Image’) {
steps {
script {
sh """
docker run -- rm -v / var / run / docker . sock
:/ var / run / docker . sock \\
aquasec / trivy : latest image -- exit - code 0
-- severity LOW , MEDIUM , HIGH , CRITICAL
\\
$ { IMAGE_NAME_CLIENT }
"""
}
}
}
stage ( ’Push Images to Docker Hub ) {steps {
script {
docker . withRegistry ( ’ ’ , " $ {DOCKERHUB_CREDENTIALS}") {
dockerImageServer . push ()
dockerImageClient . push ()
}
}
}
}
}
}