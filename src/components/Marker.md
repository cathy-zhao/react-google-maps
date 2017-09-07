## Usage

```jsx static
import { compose } from "recompose";

import {
  withGoogleMap,
  GoogleMap,
  Marker,
} from "react-google-maps";

import withScriptjs from "react-google-maps/lib/async/withScriptjs";

const MapWithAMarker = compose(
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: -34.397, lng: 150.644 }}
  >
    <Marker
      position={{ lat: -34.397, lng: 150.644 }}
    />
  </GoogleMap>
);

<MapWithAMarker
  googleMapURL="https://maps.googleapis.com/maps/api/js?v=3.exp"
  loadingElement={<div style={{ height: `100%` }} />}
  containerElement={<div style={{ height: `200px` }} />}
  mapElement={<div style={{ height: `100%` }} />}
/>
```

### Map with a Marker

```jsx
const { compose } = require("recompose");
const {
  withGoogleMap,
  GoogleMap,
  Marker,
} = require("../index");
const { default: withScriptjs } = require("../async/withScriptjs");

const MapWithAMarker = compose(
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: -34.397, lng: 150.644 }}
  >
    <Marker
      position={{ lat: -34.397, lng: 150.644 }}
    />
  </GoogleMap>
);

<MapWithAMarker
  googleMapURL="https://maps.googleapis.com/maps/api/js?v=3.exp"
  loadingElement={<div style={{ height: `100%` }} />}
  containerElement={<div style={{ height: `200px` }} />}
  mapElement={<div style={{ height: `100%` }} />}
/>
```
