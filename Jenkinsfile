node {
    stage "Checkout"
    checkout scm
    stage "Hello"
    echo "Hello, world"
    stage "Build"
    echo "Building branch ${env.BRANCH_NAME}"
    def branch = "${env.BRANCH_NAME}"
    stage "Deploy"
    if (branch == "develop") {
        echo "Deploying to Dev"
    }
    else if (branch ==~ /release\/.*/) {
        echo "Deploying to QA"
    }
    else if (branch == "master") {
        echo "Deploying to Prod"
    }
}
