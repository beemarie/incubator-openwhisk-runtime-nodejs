#
# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.
# The ASF licenses this file to You under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with
# the License.  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

FROM buildpack-deps:trusty-curl

ENV DEBIAN_FRONTEND noninteractive

# Initial update and some basics.
RUN apt-get update && apt-get install -y imagemagick && apt-get install -y unzip

ADD . /nodejsAction
# COPY the package.json to root container, so we can install npm packages a level up from user's packages, so user's packages take precedence
COPY ./package.json /
