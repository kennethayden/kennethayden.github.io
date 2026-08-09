Natural gas combustion releases CO₂ along with pollutants such as NOₓ and SO₂. Hydrogen burns to water vapor alone, making it an attractive blending agent. However, mixing hydrogen with natural gas changes how the fuel actually burns. Flame speed, heat release timing, and soot formation all shift with the blend ratio, and there is a limit to how much an engine can usefully take.

This project characterized methane-hydrogen combustion in a single-cylinder optical spark-ignition engine, a research engine with a transparent combustion chamber and a mirrored piston extension that lets a high-speed camera record the flame directly as it develops. We ran fuel mixtures across a range of hydrogen fractions and air-fuel ratios, and developed routines to process the raw cylinder pressure traces and high-speed footage into the parameters that characterize engine performance: indicated mean effective pressure, ignition delay, heat release rate, cumulative heat release, and indicated thermal efficiency. Flame color and propagation were analyzed alongside these to connect what the combustion looked like to what the sensors measured.

The analysis identified an optimal hydrogen concentration. Efficiency and power output improve as hydrogen is added, but only up to a point. Past a certain fraction the trend reverses. Hydrogen ignites more readily than methane and begins burning ahead of it, splitting one combustion event into two poorly timed ones.

Experimental setup:  
<img alt="setup" src="https://github.com/user-attachments/assets/3ac17037-a8dd-4e83-8c70-49a9f61917e3" width="85%" />

### Combustion Imaging
Pure methane against the best-performing hydrogen blend, recorded at 20 000 fps. The hydrogen flame is brighter and propagates fast and evenly, matching the higher heat release rate measured from the pressure traces.

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>Pure methane:</h4>
      <video src="https://github.com/user-attachments/assets/c1bf2112-b832-4161-8a9b-5f4f7c929b67" controls width="100%">
      Your browser does not support the video tag.
      </video>
    </td>
  <td width="50%" valign="top">
      <h4>Hydrogen content 20%:</h4>
      <video src="https://github.com/user-attachments/assets/c3915fd4-9511-401d-9147-988e4d7e80f8" controls width="100%">
      Your browser does not support the video tag.
      </video>
    </td>
  </tr>
</table>


### Data Processing
Cylinder pressure was sampled against crank angle and processed to derive the rate at which the fuel released energy through the cycle, and the total energy released by the end of it. The two graphs below show which mixture burns hardest and which extracts the most energy overall. The peak of the rate curve reveals whether that energy arrives at a useful point in the piston's travel.

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>Heat release rate:</h4>
      <img alt="hrr" src="https://github.com/user-attachments/assets/5113bf15-e56e-44af-84b5-a898703ffa72" width="100%" />
    </td>
  <td width="50%" valign="top">
      <h4>Cumulative heat release:</h4>
      <img alt="chr" src="https://github.com/user-attachments/assets/3cb00714-7499-4e7c-8e50-8c821b8e59a3" width="100%" />
    </td>
  </tr>
</table>
