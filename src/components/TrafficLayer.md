## Usage

```jsx static
import { compose, withProps } from "recompose";
import {
  withGoogleMap,
  GoogleMap,
  TrafficLayer,
} from "react-google-maps";
import withScriptjs from "react-google-maps/lib/async/withScriptjs";

const MapWithATrafficLayer = compose(
  withProps({
    googleMapURL: "https://maps.googleapis.com/maps/api/js?v=3.exp",
    loadingElement: <div style={{ height: `100%` }} />,
    containerElement: <div style={{ height: `400px` }} />,
    mapElement: <div style={{ height: `100%` }} />,
  }),
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: 41.9, lng: -87.624 }}
  >
    <TrafficLayer autoUpdate />
  </GoogleMap>
);

<MapWithATrafficLayer />
```

### Map with a TrafficLayer

```jsx
const { compose, withProps } = require("recompose");
const {
  withGoogleMap,
  GoogleMap,
  TrafficLayer,
} = require("../index");
const { default: withScriptjs } = require("../async/withScriptjs");

const MapWithATrafficLayer = compose(
  withProps({
    googleMapURL: "https://maps.googleapis.com/maps/api/js?v=3.exp",
    loadingElement: <div style={{ height: `100%` }} />,
    containerElement: <div style={{ height: `400px` }} />,
    mapElement: <div style={{ height: `100%` }} />,
  }),
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: 41.9, lng: -87.624 }}
  >
    <TrafficLayer autoUpdate />
  </GoogleMap>
);

<MapWithATrafficLayer />
```
