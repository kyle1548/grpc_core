add_executable(NodeTestPub "NodeTestPub.cpp")
target_link_libraries(NodeTestPub
  ${_CORE_LIBRARIES}
  hello_proto)
add_executable(NodeTestSub "NodeTestSub.cpp")
target_link_libraries(NodeTestSub
  ${_CORE_LIBRARIES}
  hello_proto)
add_executable(NodeTestServiceServer "NodeTestServiceServer.cpp")
target_link_libraries(NodeTestServiceServer
  ${_CORE_LIBRARIES}
  hello_proto)
add_executable(NodeTestServiceClient "NodeTestServiceClient.cpp")
target_link_libraries(NodeTestServiceClient
  ${_CORE_LIBRARIES}
  hello_proto)