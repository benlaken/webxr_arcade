# WebXR Retro Arcade

An immersive WebXR experience that combines classic arcade games in a stunning virtual reality environment. Experience the nostalgia of 80s vector graphics with modern VR hand tracking technology.

## 🎮 Features

### Core Experience
- **Hand Tracking VR**: Fully controller-free experience designed for Meta Quest 3
- **Boids Flocking Simulation**: 50 AI-driven entities with realistic flocking behavior (optimized for Quest performance)
- **Interactive Mechanics**: Grab, toss, shake, and punch your way through the environment
- **Gesture-Based Teleportation**: Point and hold for 3 seconds to teleport (perfect for small VR spaces)

### Retro Arcade Games

#### 🚗 Battle Zone Tank Warfare (Ground Level)
- 12 wireframe tanks in epic combat
- Two-team AI battles with realistic physics
- Projectile combat with explosion effects
- Continuous respawning for non-stop action
- Safe 25+ meter distance from user

#### 🚀 Asteroids Space Battle (Sky Level)
- Classic space combat 30+ meters overhead
- Triangular spaceships hunting asteroids
- Authentic asteroid splitting mechanics (large → medium → small)
- 200 twinkling stars creating a beautiful starfield
- ✨ **Sporadic shooting stars** with particle trails

#### 🏍️ Tron Light Cycles (Racing Circuit)
- Two light cycles racing with authentic 90-degree turns
- Persistent light trail walls that fade over time
- Collision detection and avoidance AI
- Cyan vs Orange team colors
- Safe racing boundaries beyond user space

### Interactive Elements

#### Conway's Game of Life Monolith
- Massive 16x80 interactive light panel array
- Extends from ground to sky (12+ units tall)
- Touch panels to activate cells
- Auto-running with classic patterns (gliders, oscillators)
- Automatic pattern injection when reaching stable states

#### Ornamental Fountain System
- Constantly active voxel fountain (6 voxels/second)
- Physics-based particle system with gravity
- Grab fountain voxels to revive as new boids
- 15-second lifetime with fade effects

#### Geometric Forest
- 5 Tron-inspired wireframe trees
- Obstacle avoidance for boids
- Cyan glowing aesthetic

#### Gesture-Based Teleportation System
- **Point to Target**: Extend right index finger toward desired location
- **3-Second Hold Timer**: Visual progress indicator with shake tolerance
- **15-Meter Range**: Suitable for exploring the entire arcade environment
- **Visual Feedback**: Cyan targeting reticle and expanding progress ring
- **Particle Effects**: Satisfying teleport visual with cyan particle burst
- **Small Space Friendly**: Perfect for room-scale VR in limited physical areas

### Hand Interaction Mechanics
- **Grab & Toss**: Pinch to grab boids and toss them with physics
- **Shake to Create Predators**: Vigorous shaking transforms voxels into hunting predators
- **Punch Blast**: Make a fist and punch to create force waves that affect boids
- **Touch Interaction**: Touch Game of Life panels to toggle cell states
- **Teleportation**: Point with right hand for 3 seconds to teleport (perfect for small VR spaces)

## 🛠️ Technical Details

### Technologies Used
- **Three.js**: 3D graphics and WebGL rendering
- **WebXR**: VR and hand tracking APIs
- **JavaScript ES6+**: Modern web standards
- **Instanced Rendering**: Optimized performance for 100+ entities

### Performance Optimizations
- Frame-rate based updates for smooth VR experience
- Instanced mesh rendering for boids and particles
- Efficient particle systems with automatic cleanup
- Optimized collision detection with spatial partitioning

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
- **Pinch**: Grab boids or fountain voxels
- **Fist**: Create punch force blasts
- **Point**: Touch Game of Life panels OR hold for 3 seconds to teleport
- **Shake**: Transform held voxels into predators

### Desktop Fallback
- **Mouse**: Look around
- **Click**: Basic interaction (limited functionality)

## 🎨 Visual Style

The entire experience embraces 80s retro aesthetics:
- **Wireframe Geometry**: Classic vector graphics style
- **Neon Colors**: Cyan, orange, green, and red glowing elements
- **Particle Effects**: Explosion and trail systems
- **Tron-Inspired**: Geometric shapes and light trails
- **Dark Environment**: Space-like atmosphere with selective lighting

## 🔧 Customization

Key parameters can be adjusted in the code:
- `TANK_COUNT`: Number of battle tanks
- `ASTEROID_COUNT`: Space battle density
- `CYCLE_SPEED`: Light cycle racing speed
- `SHOOTING_STAR_SPAWN_RATE`: Meteor frequency
- `GRID_SIZE_X/Y`: Game of Life dimensions

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

- Inspired by classic arcade games: Battle Zone, Asteroids, and Tron
- Conway's Game of Life cellular automaton
- Three.js community for excellent WebXR examples
- Meta for WebXR hand tracking technology

---

**Built with ❤️ for the VR community**

*Experience the future of retro gaming in virtual reality!*