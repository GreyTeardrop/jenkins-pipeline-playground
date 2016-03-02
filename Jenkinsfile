node {
    stage 'Checkout'
    checkout scm

    stage 'Hello'
    echo 'Hello, world'

    stage 'Build'
    String branch = env.BRANCH_NAME
    echo "Building branch $branch"

    if (branch == 'develop') {
        stage 'Deploy'
        deployToDev()
    }
    else if (branch ==~ /release\/.*/) {
        stage 'Deploy'
        deployToQa()
    }
    else if (branch == 'master') {
        stage 'Deploy'
        deployToProd()
    }
}

def deployToDev() {
    echo 'Deploying to Dev'
}

def deployToQa() {
    echo 'Deploying to QA'
}

def deployToProd() {
    echo 'Deploying to QA'
}
