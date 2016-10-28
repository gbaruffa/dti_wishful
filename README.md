# Dvb-Tx-Iris Project

Iris is a software architecture for building highly reconfigurable radio networks using a component-based design. The architecture comprises two repositories - Iris_Core and Iris_Modules. Iris_Core contains the core part of the architecture such as parsers, managers and engines. Iris_Modules contain the components which can be used to create your software radio such as PHY-layer components and radio controllers. Dvb-Tx-Iris is an extension set of modules that allow to create DVB-T modulators.

## Description

The Iris architecture offers support for all layers of the network stack and provides a platform for the development of not only reconfigurable point-to-point radio links but complete networks of reconfigurable radios. Individual radios are described using an XML document. This lists the components which comprise the radio, gives the values to be used for their parameters and describes the connections between them.

Iris was originally developed by CTVR, The Telecommunications Research Centre, based at University of Dublin, Trinity College. In 2013, it was released under the LGPL v3 license and is currently managed by Software Radio Systems (http://www.softwareradiosystems.com).

## Getting Started

The installation guide can be found in the DOC folder, available after compilation.
Read the INSTALLATION section for further information.
After installation is carried out, run an example:

* cd examples/dvbt
* dd if=/dev/urandom of=mux4800000.ts bs=1M count=10
* iris -f config.iris dvbt1chain_ofdmmod_filter_spectrum.xml 

## Requirements

Required:
* CMake 2.6 or later - http://www.cmake.org/
* Boost 1.46 or later - http://www.boost.org/
* Iris_Core
* Iris_Modules
* FFTW - http://www.fftw.org/ (For FFT transforms)

Optional:
* Qt 4.8 - http://qt-project.org/ (For graphical widgets)
* Qwt 6 - http://qwt.sourceforge.net/ (For graphical widgets)
* UHD - http://code.ettus.com/redmine/ettus/projects/uhd/wiki (For using USRP hardware)
* Liquid-DSP - https://github.com/jgaeddert/liquid-dsp (For some PHY components)
* Google Protocol Buffers - https://developers.google.com/protocol-buffers/ (For some Stack components)
* Python - http://www.python.org/ (For PythonPlotter widget)
* Matlab (For MatlabTemplate PHY component, MatlabPlotter widget)
* Doxygen (for the documentation)

## Installation

* Use SVN to check out the main repository branch with the communicated credentials
** svn checkout http://dante.diei.unipg.it/svn/dti_wishful
* cd dti_wishful
* mkdir build
* cd build
* cmake ..
* make
* make test
* make benchmark
* sudo make install
* cd ..
* cd doc
* doxygen

## Where To Get Help

* Redmine: http://www.softwareradiosystems.com/redmine/projects/iris
* Iris-discuss mailing list: http://www.softwareradiosystems.com/mailman/listinfo/iris-discuss
* Iris blog: http://irissoftwareradio.wordpress.com

## License

Dvb-Tx-Iris is licensed under LGPL v3. For more information see LICENSE.

