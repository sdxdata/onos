COMPILE_DEPS = CORE_DEPS + JACKSON + [
    "@javax_ws_rs_api//jar",
    "//utils/rest:onlab-rest",
    "//drivers/utilities:onos-drivers-utilities",
    "//protocols/rest/api:onos-protocols-rest-api",
]

TEST_DEPS = TEST_ADAPTERS + [
    "//core/api:onos-api-tests",
]

BUNDLES = [
    ":onos-drivers-dellrest",
    "//drivers/utilities:onos-drivers-utilities",
]

osgi_jar_with_tests(
    resources = glob(["src/main/resources/**"]),
    resources_root = "src/main/resources",
    test_deps = TEST_DEPS,
    deps = COMPILE_DEPS,
)

onos_app(
    app_name = "org.onosproject.drivers.dellrest",
    category = "Drivers",
    description = "Adds support for Dell Networks devices using REST.",
    included_bundles = BUNDLES,
    required_apps = ["org.onosproject.restsb"],
    title = "Dell Networks REST Drivers",
    url = "http://onosproject.org",
)
