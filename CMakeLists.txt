# Copyright 2018-2020 Peter Dimov
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5...3.16)

project(boost_asio VERSION "${BOOST_SUPERPROJECT_VERSION}" LANGUAGES CXX)

add_library(boost_asio INTERFACE)
add_library(Boost::asio ALIAS boost_asio)

target_include_directories(boost_asio INTERFACE include)

target_link_libraries(boost_asio
  INTERFACE
    Boost::config
    Boost::winapi
)


