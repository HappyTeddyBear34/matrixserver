project(server_FPGA_RPISPI)

add_executable(server_FPGA_RPISPI main.cpp)
target_link_libraries(server_FPGA_RPISPI server FPGARenderer)

target_compile_definitions(server_FPGA_RPISPI PUBLIC BOOST_LOG_DYN_LINK)

install(TARGETS server_FPGA_RPISPI
        RUNTIME
        DESTINATION /home/pi/
        COMPONENT application
        )