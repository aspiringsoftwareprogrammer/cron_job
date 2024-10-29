multibranchPipelineJob('multibranch/main') {
    // Description of the job
    description('An example multibranch pipeline job created via Jenkins Job DSL')

    // Set branch sources
    branchSources {
        git {
            id('unique-branch-source-id') // Unique identifier for branch source
            remote('https://github.com/aspiringsoftwareprogrammer/testing_cron_auto_triggers.git') // Replace with your repository URL
            includes('*') // Define which branches to include
        }
    }

    // Set branch discovery options
    orphanedItemStrategy {
        discardOldItems {
            numToKeep(10) // Keep up to 10 recent builds
            daysToKeep(30) // Retain builds for up to 30 days
        }
    }
}
