Libav with CUDA accelerated VP8 encoder
=====

### Developed by Italtel and Universita' degli Studi di Milano, 2015-6
Alessandro Petrini, Pietro Paglierani, Giuliano Grossi, Federico Pedersini

Libav is a collection of libraries and tools to process multimedia content
such as audio, video, subtitles and related metadata.

This version enables the NVidia CUDA accelerated encoder provided by the fork of the official libvpx at https://github.com/Topopiccione/libvpx . All the other libraries were not modified.


## Build Instructions
Directory t_build has been already per-configured for building on x86_64 Linux, so that the
```
make
```
command would ideally be enough for compiling and linking.

This program requires NVidia CUDA SDK 8.0 for compiling, so that NVidia nvcc must be present in the system under the directory:
/usr/local/cuda-8.0/bin/
otherwise the files
```
t_build/config.mak
```
must be modified accordingly accordingly.

It is possible to create a working makefile from scratch using the standard configure by following the instruction on BUILD_INSTR.txt


## Compiled binary

As now, we are not providing a compiled binary package.


## Usage
the command line options
```
-cuda_me_enabled 1
-cuda_me_enabled 2
-cuda_me_enabled 3
```
enables the GPU acceleration for VP8 encoding only; mode 1 is the fastest and less accurate, while 2 is an intermediate level, and 3 is the most accurate.


## Documentation

Online documentation for the accelerated VP8 encoder developed by Italtel and Universita' degl studi di Milano is available at https://github.com/Topopiccione/libvpx


## Contacts

Alessandro Petrini (UNIMI) - email: alessandro.petrini@unimi.it

Pietro Paglierani (ITALTEL) - email: pietro.paglierani@italtel.com

Giuliano Grossi (UNIMI) - email: grossi@di.unimi.it

Federico Pedersini (UNIMI) - email: pedersini@di.unimi.it


# DISCLAIMER

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## License

Libav codebase is mainly LGPL-licensed with optional components licensed under
GPL. Please refer to the LICENSE file for detailed information.
