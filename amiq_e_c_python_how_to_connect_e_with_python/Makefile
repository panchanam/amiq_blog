# /******************************************************************************
# * (C) Copyright 2019 AMIQ Consulting
# *
# * Licensed under the Apache License, Version 2.0 (the "License");
# * you may not use this file except in compliance with the License.
# * You may obtain a copy of the License at
# *
# * http://www.apache.org/licenses/LICENSE-2.0
# *
# * Unless required by applicable law or agreed to in writing, software
# * distributed under the License is distributed on an "AS IS" BASIS,
# * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# * See the License for the specific language governing permissions and
# * limitations under the License.
# *
# * MODULE:      BLOG
# * PROJECT:     How To Connect e-Language with Python
# * Description: This is a code snippet from the Blog article mentioned on PROJECT
# * Link:        https://www.amiq.com/consulting/2019/04/25/how-to-connect-e-language-with-python/
# *******************************************************************************/

run_e: build_e
	@export LD_LIBRARY_PATH=$(shell pwd)
	irun amiq_top.e amiq_top.sv amiq_mux2_1.v

build_e:
	irun -f ${PROJ_HOME}/sim/sim.options
	
clean:
	find . -type f -not \( -name '*.sv' -or -iname '*.sh' -or -iname '*.v' -or -iname '*.py' -or -iname '*.cc' -or -iname 'Makefile' -or -iname '*.options' -or -iname '*.e' \) -delete
	find . -type d -not \( -name 'sim' -or -iname 'sim/*' -or -name '.*' \) -exec rm -rf {} +
	
.PHONY: clean

