add_executable(grpccore "Master.cpp")
target_link_libraries(grpccore
registration_grpc_proto
connection_grpc_proto
${_REFLECTION}
${_GRPC_GRPCPP}
${_PROTOBUF_LIBPROTOBUF})

target_public_headers(grpccore 
"${CMAKE_SOURCE_DIR}/include/NodeHandler.h"
"${CMAKE_SOURCE_DIR}/include/Timer.h"
"${CMAKE_SOURCE_DIR}/include/TCPSocket.h"
"${CMAKE_SOURCE_DIR}/include/Master.h"
)

INSTALL(TARGETS grpccore
RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
INCLUDES DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
)
