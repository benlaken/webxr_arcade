# WebXR Boids Interactive

An immersive WebXR experience featuring intelligent boids flocking simulation optimized for **120fps performance** on Meta Quest 3. Experience responsive hand tracking with reliable gesture detection, teleportation, and force punch mechanics in a clean, performance-focused virtual environment.

## 🎮 Features

### Core Experience
- **Hand Tracking VR**: Fully controller-free experience designed for Meta Quest 3 at 120fps
- **Boids Flocking Simulation**: 25 AI-driven entities with realistic flocking behavior
- **Interactive Mechanics**: Grab, toss, shake, and punch your way through the environment
- **Gesture-Based Teleportation**: Point and hold for 3 seconds to teleport (perfect for small VR spaces)

### Interactive Elements

#### 🚀 Asteroids Space Battle (Sky Level)
- Classic space combat 30+ meters overhead  
- Triangular spaceships hunting asteroids at optimized speeds
- Authentic asteroid splitting mechanics (large → medium → small)
- 200 twinkling stars creating a beautiful starfield
- ✨ **Sporadic shooting stars** with particle trails
- **Recently optimized**: 30% speed reduction for better visibility and tracking

#### Ornamental Fountain System
- Constantly active voxel fountain (4 voxels/second)
- Physics-based particle system with gravity
- Grab fountain voxels to revive as new boids
- 8-second lifetime with fade effects

#### Gesture-Based Teleportation System
- **Point to Target**: Extend right index finger toward desired location
- **3-Second Hold Timer**: Visual progress indicator with shake tolerance
- **15-Meter Range**: Suitable for exploring the entire environment
- **Visual Feedback**: Cyan targeting reticle and expanding progress ring
- **Particle Effects**: Satisfying teleport visual with cyan particle burst
- **Small Space Friendly**: Perfect for room-scale VR in limited physical areas

### Hand Interaction Mechanics
- **Grab & Toss**: Pinch to grab boids and toss them with physics
- **Shake to Create Predators**: Vigorous shaking transforms voxels into hunting predators  
- **Punch Blast**: Make a fist and punch to create force waves that affect boids
  - *Recently fixed*: Reliable detection with startup stabilization and velocity smoothing
  - *Debug overlay*: Real-time punch counter and velocity tracking
- **Teleportation**: Point with right hand for 3 seconds to teleport (perfect for small VR spaces)
  - *Recently improved*: Enhanced XR reference space handling with player rig system

## 🛠️ Technical Details

### Technologies Used
- **Three.js**: 3D graphics and WebGL rendering
- **WebXR**: VR and hand tracking APIs
- **JavaScript ES6+**: Modern web standards
- **Instanced Rendering**: Optimized performance for 100+ entities

### Performance Optimizations (120fps Quest 3)
- **Aggressive 120fps optimizations**: LOD system, temporal update spreading, spatial partitioning
- **Dynamic quality scaling**: Real-time FPS monitoring with automatic quality adjustment
- **Instanced mesh rendering**: Optimized for boids and particles with reduced update frequency
- **Object pooling**: Eliminates garbage collection overhead for particles
- **Frustum culling**: Skip updates for off-screen objects
- **Simplified materials**: MeshBasicMaterial only for maximum shader performance
- **Foveated rendering**: Quest 3 specific optimizations with reduced resolution scaling
- **Hand tracking stabilization**: Velocity smoothing and startup grace periods prevent false positives
- **VR debug overlay**: Large, comprehensive debug panel for in-VR troubleshooting

### Browser Compatibility
- **Primary**: Meta Quest 3 native browser
- **Secondary**: Any WebXR-compatible browser
- **Fallback**: Desktop mouse controls for development

## 🚀 Getting Started

### Live Demo
Visit: `https://benlaken.github.io/webxr_arcade/`

### Local Development
1. Clone the repository:
   ```bash
   git clone https://github.com/benlaken/webxr_arcade.git
   cd webxr_arcade
   ```

2. Serve locally (required for WebXR):
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   ```

3. Access at `http://localhost:8000` or your local server URL

### VR Setup
1. Put on your Meta Quest 3 headset
2. Open the browser
3. Navigate to the live demo URL
4. Click "Enter VR" when prompted
5. Enjoy the retro arcade experience!

## 🎯 Controls

### Hand Gestures
- **Pinch**: Grab boids or fountain voxels (thumb and index finger close)
- **Fist**: Create punch force blasts (2 of 3 fingers curled, with fast movement)
- **Point**: Hold for 3 seconds to teleport (index extended, others curled)
- **Shake**: Transform held voxels into predators (vigorous hand movement while holding)

### Desktop Fallback
- **Mouse**: Look around
- **Click**: Basic interaction (limited functionality)

## 🎨 Visual Style

The experience embraces clean, performance-focused aesthetics:
- **Wireframe Geometry**: Classic vector graphics style
- **Neon Colors**: Cyan, orange, and green glowing elements
- **Particle Effects**: Explosion and trail systems
- **Minimalist Design**: Focused on core interactive elements
- **Dark Environment**: Space-like atmosphere with selective lighting

## 🆕 Recent Improvements

### Hand Tracking Reliability  
- **Startup stabilization**: 60-frame grace period prevents false punch detection on app load
- **Velocity smoothing**: Lerp-based position smoothing handles tracking loss gracefully
- **Improved fist detection**: 2-of-3 finger algorithm with optimized thresholds
- **Player rig system**: Proper VR coordinate handling for teleportation

### Performance & Visibility
- **Space battle optimization**: 30% speed reduction for asteroids and spaceships
- **Debug overlay expansion**: Larger debug panel (800x600) fits all information
- **Enhanced logging**: Comprehensive console output for troubleshooting

### Bug Fixes
- **Punch detection**: Eliminated startup auto-activation and cooldown conflicts  
- **Web worker cleanup**: Removed incomplete async code causing crashes
- **Reference space handling**: Fixed head/hand separation during teleportation

## 🔧 Customization

Key parameters can be adjusted in the code:
- `initialBoidCount`: Number of boids (default: 25)
- `ASTEROID_COUNT`: Space battle density (default: 6)
- `ASTEROID_SPEED`: Asteroid movement speed (default: 17.5, recently reduced 30%)
- `SPACESHIP_SPEED`: Spaceship movement speed (default: 5.6, recently reduced 30%)
- `SHOOTING_STAR_SPAWN_RATE`: Meteor frequency
- `fountainSpawnRate`: Fountain voxel generation rate
- `TARGET_FRAME_RATE`: Performance target (default: 120fps)
- `currentQualityLevel`: Dynamic quality scaling factor

## 📱 Deployment

This project is deployed using GitHub Pages for:
- ✅ Free HTTPS hosting (required for WebXR)
- ✅ Automatic deployments on git push
- ✅ High performance CDN
- ✅ Perfect Quest 3 compatibility

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test in VR (especially Quest 3)
5. Submit a pull request

## 📄 License

MIT License - Feel free to use and modify for your own projects!

## 🙏 Acknowledgments

- Inspired by classic arcade games: Asteroids and boids flocking algorithms
- Craig Reynolds' original boids simulation research
- Three.js community for excellent WebXR examples
- Meta for WebXR hand tracking technology

---

**Built with ❤️ for the VR community**

*Experience intelligent boids flocking at 120fps in virtual reality!*