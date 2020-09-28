The Basic React Code for an Event In Focus
===========================================
    .. code-block:: javascript

     return (
          <div className="showEventWrapper">
            <div className="showEvent">
              <div className="vaporwaveBar">
                <div className="vbar-buttons">
                  <button className="vaporwaveBarContents">
                    <img
                        src={require("../images/media_player_stream_no.png")}
                        alt="alt"
                    />
                  </button>
                  <button className="vaporwaveBarContents">
                    <img
                        src={require("../images/button-left-v.svg")}
                        alt="Error"
                        className="leftRight"
                    />
                  </button>
                  <button className="vaporwaveBarContents">
                    <img src={require("../images/button-right-v.svg")} alt="burr" />
                  </button>
                </div>
              </div>
              <div id="header" className="eventHeader">
                <h2 id="eventHeader-text">
                  {this.props.header}
                </h2>
                <div id="locationTimeWrapper"/>
              </div>
              <div className="eventBody">
                <img
                    className="eventBody-image"
                    id="eventBody-image1"
                    src={this.props.images[0]}
                    alt={""}
                />
                <p  className="eventBody-text">
                  <img
                      className="eventBody-image"
                      id="eventBody-image2"
                      src={this.props.images[1]}
                      alt=""
                  />
                  {this.props.body}
                </p>
              </div>
              <div className="event-citation">
                <p id="event-citation-text">{this.props.citation[0]}</p>

                <p id="event-citation-text">,</p>

                <p id="event-citation-text" style={{ marginLeft: 5 }}>
                  {this.props.citation[1]}
                </p>
              </div>
            </div>
          </div>
      );

Props
----------
* Style: Which styling should we us
* Header: Summary of the event
* Body: The text of the event, as one paragraph
* Images: The src/url of the pics we want to display
 * Currently we only support two, but this will change soon


Default CSS
-----------
Tinker around with EventInFocus.css



The Basic Unique Styling Code for an Event In Focus
===================================================
    .. code-block:: css

      const STYLEPROPGOESHEREDiv = {
        background: '#BACKGROUND EVENT COLOR GOES HERE',
        border: '2px solid #ffffff'
      }
      const STYLEPROPGOESHEREText = {
        fontFamily: "CUSTOM FONT GOES HERE",
        color: 'TEXT EVENT COLOR GOES HERE ',
        marginLeft: 5,
        fontSize: '1rem',
      }

      const STYLEPROPGOESHEREBar = {
        color: 'BUTTON COLOR FOR BAR GOES HERE',
        backgroundColor: 'BACKGROUND COLOR FOR BAR GOES HERE',
      }

Then apply these styles in an if statement in EventInFocus.js
----------------------------------------------------------------------
    .. code-block:: javascript

     else if (this.props.style === "STYLE PROP GOES HERE") {
      return (
      ...
      )
     },







