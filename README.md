[output_1]: img/output_1.png
[output_2]: img/output_2.png

# Extended Kalman Filter Project
Self-Driving Car Engineer Nanodegree Program

---

## Summary

This repository contains a C++ implementation of an Extended Kalman Filter. It has been implemented as part of the Udacity Self-Driving Car Engineer Nanodegree Program.

### Data

There are two data files in the repository. Each line in the data file represents either a lidar or radar measurement marked by "L" or "R" on the starting line. The next following values are either the 2 lidar position measurements (x,y) or the 3 radar position measurements (rho, phi, rho_dot). The next value is then the time stamp and then finally the ground truth values for x, y, vx, vy.

#### NOTE:

In Data 2, the starting lidar measurements for x, y are both zero, and this special case can create problems for both the EKF and UKF lidar update states, in particular for the EKF when calculating the Jacobian. One way to catch for this is to observe when both px, py are zero and instead set them to some small floating value.

### Evaluation

Data file: sample-laser-radar-measurement-data-1.txt

![output_1.png][output_1]

Data file: sample-laser-radar-measurement-data-2.txt

![output_2.png][output_2]


## Dependencies

* cmake >= 3.5
 * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make` 
   * On windows, you may need to run: `cmake .. -G "Unix Makefiles" && make`
4. Run it: `./ExtendedKF path/to/input.txt path/to/output.txt`. You can find
   some sample inputs in 'data/'.
    - eg. `./ExtendedKF ../data/sample-laser-radar-measurement-data-1.txt output.txt`

