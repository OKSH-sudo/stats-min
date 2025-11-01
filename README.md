# Compute Minimum Values in ndarrays with stats-min

![npm](https://img.shields.io/npm/v/stats-min) ![GitHub](https://img.shields.io/github/license/OKSH-sudo/stats-min) ![GitHub stars](https://img.shields.io/github/stars/OKSH-sudo/stats-min) ![GitHub forks](https://img.shields.io/github/forks/OKSH-sudo/stats-min)

## Overview

The `stats-min` library allows you to compute the minimum value along one or more dimensions of an ndarray. This tool is essential for anyone working with numerical data, statistics, or mathematical computations in JavaScript.

### Features

- **Multi-dimensional Support**: Compute minimum values across multiple dimensions of ndarrays.
- **Fast Performance**: Optimized for speed, ensuring quick calculations even with large datasets.
- **Simple API**: Easy to use with a straightforward interface, making it accessible for both beginners and experienced developers.

## Installation

You can install `stats-min` via npm. Run the following command in your terminal:

```bash
npm install stats-min
```

## Usage

To use `stats-min`, you first need to import it into your project. Here’s a simple example:

```javascript
const statsMin = require('stats-min');

// Create an ndarray
const ndarray = require('ndarray');
const data = ndarray(new Float32Array([1, 2, 3, 4, 5]), [5]);

// Compute the minimum value
const minValue = statsMin(data);
console.log('Minimum Value:', minValue); // Outputs: Minimum Value: 1
```

### API

#### `statsMin(array, axis)`

- **array**: The input ndarray.
- **axis**: (Optional) The dimension along which to compute the minimum. If not specified, the minimum is computed over the entire array.

**Example**:

```javascript
const minValue = statsMin(data, 0);
console.log('Minimum Value along axis 0:', minValue);
```

## Topics Covered

This library is relevant to several topics in mathematics and statistics, including:

- **Domain**: The range of values that can be processed.
- **Extent**: The total number of dimensions in an ndarray.
- **Extremes**: Finding the minimum and maximum values in datasets.
- **Statistics**: Essential for data analysis and interpretation.

## Contributing

Contributions are welcome! If you want to improve the library, feel free to fork the repository and submit a pull request. Please ensure that your code follows the existing style and includes appropriate tests.

### Steps to Contribute

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push to your branch.
5. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

You can find the latest releases of `stats-min` [here](https://github.com/OKSH-sudo/stats-min/releases). Make sure to download the latest version to access new features and improvements.

### Versioning

The library follows semantic versioning. You can track the changes in each release through the releases section.

## Examples

### Example 1: Basic Minimum Calculation

```javascript
const ndarray = require('ndarray');
const statsMin = require('stats-min');

const data = ndarray(new Float32Array([10, 20, 30, 5, 15]), [5]);
const minValue = statsMin(data);
console.log('Minimum Value:', minValue); // Outputs: Minimum Value: 5
```

### Example 2: Minimum Calculation Along a Specific Axis

```javascript
const ndarray = require('ndarray');
const statsMin = require('stats-min');

const data = ndarray(new Float32Array([10, 20, 30, 5, 15, 25]), [2, 3]);
const minValueAxis0 = statsMin(data, 0);
console.log('Minimum Value along axis 0:', minValueAxis0); // Outputs: Minimum Value along axis 0: [5, 15, 25]
```

## Performance Benchmarking

To evaluate the performance of `stats-min`, we can compare it with other libraries. Below is a simple benchmark setup:

```javascript
const { performance } = require('perf_hooks');
const statsMin = require('stats-min');
const otherLibrary = require('other-library');

const data = ndarray(new Float32Array(1000000).fill(Math.random()), [1000, 1000]);

const startStatsMin = performance.now();
statsMin(data);
const endStatsMin = performance.now();

const startOtherLibrary = performance.now();
otherLibrary.min(data);
const endOtherLibrary = performance.now();

console.log(`stats-min: ${endStatsMin - startStatsMin} ms`);
console.log(`other-library: ${endOtherLibrary - startOtherLibrary} ms`);
```

## FAQ

### What is an ndarray?

An ndarray (n-dimensional array) is a data structure that allows you to store and manipulate multi-dimensional data efficiently. It is widely used in numerical computing and data analysis.

### Can I use `stats-min` in the browser?

Yes, `stats-min` can be used in both Node.js and browser environments. You may need to use a bundler like Webpack or Browserify for browser usage.

### What if I encounter issues?

If you encounter any issues or bugs, please check the [issues section](https://github.com/OKSH-sudo/stats-min/issues) of the repository. You can also create a new issue to report any problems.

## Community

Join our community of developers and users! Share your experiences, ask questions, and connect with others who are using `stats-min`. You can find us on:

- [GitHub Discussions](https://github.com/OKSH-sudo/stats-min/discussions)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/stats-min)

## Changelog

Keep track of all changes made to the library in the [CHANGELOG](CHANGELOG.md). This file contains details about new features, bug fixes, and other updates.

## Additional Resources

For more information on ndarrays and their usage, check out the following resources:

- [ndarray Documentation](https://github.com/nanostack/ndarray)
- [JavaScript Math Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

## Explore More

Explore the full potential of `stats-min` and see how it can enhance your data analysis tasks. Don't forget to visit our [Releases](https://github.com/OKSH-sudo/stats-min/releases) section for the latest updates and features.

## Acknowledgments

Special thanks to all contributors and the community for their support and feedback. Your contributions help improve the library and make it more useful for everyone.

## Contact

For any inquiries or suggestions, feel free to reach out via the GitHub repository or through the community channels mentioned above. Your feedback is valuable in shaping the future of `stats-min`.