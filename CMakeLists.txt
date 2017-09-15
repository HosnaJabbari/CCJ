# Ian Wark July 6 2017

cmake_minimum_required(VERSION 3.1)
project(CCJ)


# ==============================
# DANGLE MODE
# Sebastian Will, Sep 7, 2017
# control energy contribution of dangles;
# the mode number models Vienna RNA's -d option
#
# NOTE: this feature is not completely implemented; set to 1 to get
# consistent behavior like in original simfold/CCJ
add_definitions("-DDANGLE_MODE=2")


# set SIMFOLD_HOME to simfold folder so CCJ binary can find it
set(SIMFOLD_HOME ${CMAKE_SOURCE_DIR}/simfold)
add_subdirectory(simfold)
add_subdirectory(Sparse_CCJ)
add_subdirectory(Original_CCJ)
