add_subdirectory(contrib)

core_gather_headers()

gather_srcs(
  cinnapi_src
  SRCS
  nn.cc
  broadcast.cc
  transform.cc
  elementwise.cc
  reduction.cc
  op_util.cc
  custom_call.cc
  external_api_registry.cc)

cinn_cc_test(test_external_api_registry SRCS external_api_registry_test.cc DEPS
             cinncore)
