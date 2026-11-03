# Distributed under the OSI-approved BSD 3-Clause License.  See accompanying
# file Copyright.txt or https://cmake.org/licensing for details.

cmake_minimum_required(VERSION 3.31.12)

# Reject any attempt to use a toolchain file. We must not use one because
# we could be downloading it here. If the CMAKE_TOOLCHAIN_FILE environment
# variable is set, the cache variable will have been initialized from it.
unset(CMAKE_TOOLCHAIN_FILE CACHE)
unset(ENV{CMAKE_TOOLCHAIN_FILE})

# We name the project and the target for the ExternalProject_Add() call
# to something that will highlight to the user what we are working on if
# something goes wrong and an error message is produced.

project(psx_libwebp-populate NONE)



include(ExternalProject)
ExternalProject_Add(psx_libwebp-populate
                     "UPDATE_DISCONNECTED" "False" "DOWNLOAD_EXTRACT_TIMESTAMP" "TRUE" "EXTERNALPROJECT_INTERNAL_ARGUMENT_SEPARATOR" "URL" "https://codeload.github.com/webmproject/libwebp/tar.gz/4fa21912338357f89e4fd51cf2368325b59e9bd9" "URL_HASH" "SHA256=923f3382a47a2af185c3240c954cf004428b237bd7317413a95146d01eb4b94b" "SOURCE_SUBDIR" "_psx_no_automatic_subdirectory"
                    SOURCE_DIR          "C:/Recompdev/MagicalMysteryMallRecomp/build-repaired/_deps/psx_libwebp-src"
                    BINARY_DIR          "C:/Recompdev/MagicalMysteryMallRecomp/build-repaired/_deps/psx_libwebp-build"
                    CONFIGURE_COMMAND   ""
                    BUILD_COMMAND       ""
                    INSTALL_COMMAND     ""
                    TEST_COMMAND        ""
                    USES_TERMINAL_DOWNLOAD  YES
                    USES_TERMINAL_UPDATE    YES
                    USES_TERMINAL_PATCH     YES
)


