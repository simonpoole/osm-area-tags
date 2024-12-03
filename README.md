## OpenStreetMap tags that imply "area" semantics

A simple OSM closed (that is first node is the same as the last node) _way_ can either represent a "polygon" that is a simple area with no holes or a linear feature that loops. While area semantics can be forced by adding an _area=yes_ tag, most of the time area semantics are implied by the tagging, or rather the kind of object the OSM element represents.

It should be noted that there are degenerate cases in which the tagging can imply both, for example a closed way that is tagged both as a roundabout and a garden. These should be avoided, and can easily be by using a second way with the same nodes as the original one.

Objects modeled as OSM multi-polygons always have area semantics.

This is based on data from https://github.com/ideditor/id-area-keys as a starting point that extracts the information from the iD presets and from iD source code, but supports both
_key_ implies area semantics and certain values don't, and the opposite when _key_ normally implies linear, but certain values have area semantics.

Yes, this is a bad case of https://xkcd.com/927/

 



