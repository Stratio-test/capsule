@Library('libpipelines') _

hose {
    EMAIL = 'eos@stratio.com'
    BUILDTOOL = 'make'
    DEVTIMEOUT = 30
    ANCHORE_POLICY = "production"
    VERSIONING_TYPE = 'stratioVersion-3-3'
    UPSTREAM_VERSION = '0.1.3'
    DEPLOYONPRS = true
    GRYPE_TEST = true

    DEV = { config ->
        doDocker(conf:config, image:'capsule')
        doHelmChart(conf: config, helmTarget: "chart")
    }
}
