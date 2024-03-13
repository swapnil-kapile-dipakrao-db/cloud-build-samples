# Copyright 2020 Google LLC
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

# [START cloudbuild_quickstart_build_dockerfile]
FROM python:3.9

# Copying my app to the image
ENV APP_HOME /app
WORKDIR $APP_HOME
COPY . ./

# Install production dependencies form the requirements.txt file
RUN pip install -r requirements.txt

# Startup command to serve our app
CMD exec gunicorn --bind :$PORT --workers 1 --threads 8 main:app
# [END cloudbuild_quickstart_build_dockerfile]
