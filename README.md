#LaserPulse

LaserPulse is a class for storing and handling laser pulses.
Pulses can be defined in either time or frequency domain.
Afterwards, both domains are automatically synchronized.

#####Functionalities:
 * **Automatic Fourier Transform:**
   When a pulse is modified in time domain the spectral field is
   automatically updated using fft, and vice versa.
 * **Physical Quantities:**
   Pulse duration, bandwidth, central frequency, and other properties 
   of the pulse are automatically calculated.
 * **Mathematical Operators:**
   The LaserPulse class supports arithmetic operations, convolutions and
   calculation of higher harmonics. The operators are applied in time
   domain, so for instance p1*p2 is a multiplication in time domain and
   a convolution in frequency domain. See the example files for more
   information.
 * **Pulse Trains:**
   Multiple sub-pulses are stored as columns in a multidimensional
   arrays. Pulse parameters, like pulse duration and bandwidth, are
   calculated using the total pulse intensity, that is
   sum(abs(complexfield).^2,2) for a 2D array. This can be useful for
   storing the field components for different orthogonal polarizations.

#####Installation:
 * Automatic Installation:
    From matlab: go to the folder where the LaserPulse is located (for example 
    'cd LaserPulseClass') and run the installer script 'install_LaserPulse.m'.
 * Manual Installation:
     For installing the **LaserPulse** class, just include its parent folder
   in the matlab search path or, alternatively, copy the '@LaserPulse' 
   folder in a folder which is in the matlab search path.
     For using the additional utilities and example files, also add the
   'utilities' and 'examples' folders to the matlab search path.
     If the folder with the LaserPulse manual is not present, generate it
   using the matlab 'publish' function. See 'install_LaserPulse.m' for an example.



#####Copyright:

Copyright (C) 2015 Alberto Comin, LMU Muenchen.

LaserPulse is free software: you can redistribute it and/or modify it
under the terms of the GNU General Public License as published by the
Free Software Foundation, either version 3 of the License, or (at your
option) any later version. LaserPulse is distributed in the hope that
it will be useful, but WITHOUT ANY WARRANTY; without even the implied
warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See
the GNU General Public License for more details. You should have
received a copy of the GNU General Public License along with
LaserPulse.  If not, see <http://www.gnu.org/licenses/>.
