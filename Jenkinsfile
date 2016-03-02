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
        echo 'Deploying to Dev'
    }
    else if (branch ==~ /release\/.*/) {
        stage 'Deploy'
        echo 'Deploying to QA'
    }
    else if (branch == 'master') {
        stage 'Deploy'
        echo 'Deploying to Prod'
    }
}
