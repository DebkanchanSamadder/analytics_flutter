# @segment/analytics_plugin_adjust

`DestinationPlugin` for [Adjust](https://www.adjust.com/). Wraps [`adjust_sdk`](https://pub.dev/packages/adjust_sdk).

## Installation

Manually add this package to your `pubspec.yaml` file.

```yaml
dependencies:
  analytics_plugin_adjust:
    git:
      url: https://github.com/segmentio/analytics_flutter
      ref: main
      path: packages/plugins/plugin_adjust
```

## Usage

Follow the [instructions for adding plugins](https://github.com/segmentio/analytics_flutter_#adding-plugins) on the main Analytics client:

In your code where you initialize the analytics client call the `.add(plugin)` method with an `AdjustDestination` instance.

```dart
import 'package:analytics/analytics.dart';
import 'package:analytics_plugin_adjust/plugin_adjust.dart'
    show AdjustDestination;

const writeKey = 'SEGMENT_API_KEY';

class _MyAppState extends State<MyApp> {
  Analytics.init(Configuration(writeKey));

  @override
  void initState() {
    // ...

    Analytics.instance
        .addPlugin(AdjustDestination());
  }
}
```

## Support

Please use Github issues, Pull Requests, or feel free to reach out to our [support team](https://segment.com/help/).

## Integrating with Segment

Interested in integrating your service with us? Check out our [Partners page](https://segment.com/partners/) for more details.

## License

```
MIT License

Copyright (c) 2023 Segment

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
