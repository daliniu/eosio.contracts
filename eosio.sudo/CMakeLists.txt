add_executable(eosio.sudo.wasm ${CMAKE_CURRENT_SOURCE_DIR}/src/eosio.sudo.cpp)
target_include_directories(eosio.sudo.wasm
   PUBLIC 
   ${CMAKE_CURRENT_SOURCE_DIR}/include)

set_target_properties(eosio.sudo.wasm
   PROPERTIES
   RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/bin/eosio.sudo")

configure_file("${CMAKE_CURRENT_SOURCE_DIR}/abi/eosio.sudo.abi" "${CMAKE_CURRENT_SOURCE_DIR}/bin/eosio.sudo" COPYONLY)
#install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/ DESTINATION ${WASM_ROOT}/eosio.wasmsdk/include)
