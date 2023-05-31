cmake_minimum_required(VERSION 3.20.0 FATAL_ERROR)

project(docolechat-server)

add_executable(docolechat-client)

find_package(Boost )

set(sources 
	src/main.cpp
	src/chat_message.hpp)

target_sources(docolechat-client PRIVATE ${sources})
target_include_directories(docolechat-client 
	PRIVATE
		src)

target_link_directories(docolechat-client PRIVATE Boost::boost)