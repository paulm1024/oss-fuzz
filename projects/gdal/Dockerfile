# Copyright 2016 Google Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
################################################################################

FROM gcr.io/oss-fuzz-base/base-builder
MAINTAINER even.rouault@spatialys.com
RUN apt-get update && apt-get install -y make autoconf automake libtool g++ zlib1g-dev libsqlite3-dev libexpat-dev liblzma-dev libxerces-c-dev libpng12-dev libgif-dev libwebp-dev libicu-dev
#   libgeos-dev libjpeg-dev libcurl4-gnutls-dev libproj-dev libxml2-dev libnetcdf-dev netcdf-bin libpoppler-dev libspatialite-dev libhdf4-alt-dev libhdf5-serial-dev  poppler-utils libfreexl-dev unixodbc-dev libepsilon-dev libpcre3-dev
# libpodofo-dev  libcrypto++-dev
RUN git clone --depth 1 https://github.com/OSGeo/gdal gdal
WORKDIR gdal
COPY build.sh $SRC/
