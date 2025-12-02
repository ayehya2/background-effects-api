# Modular Background Effects API

A lightweight, modular JavaScript library for creating stunning animated background effects. From realistic weather and seasons to futuristic tech visualizations - all controlled through a simple API.

## Features

- 🎨 **200+ Built-in Effects** - Weather, seasons, particles, environments, tech themes
- 🔌 **Modular Architecture** - Import only what you need
- 🎛️ **Simple API** - Easy to use, powerful to customize
- ⚡ **High Performance** - Optimized canvas rendering with quality controls
- 📱 **Responsive** - Adapts to any screen size
- 🎭 **Layering System** - Stack multiple effects seamlessly
- 🔄 **Smooth Transitions** - Fade between effects naturally
- 🎮 **Interactive Effects** - Mouse, click, and scroll interactions
- 📦 **Zero Dependencies** - Pure vanilla JavaScript

## Quick Start

```bash
npm install background-effects-api
```

```javascript
import BackgroundEffects from 'background-effects-api';

const bg = new BackgroundEffects({
  container: document.getElementById('app')
});

bg.add('rain', { intensity: 0.7 });
bg.add('thunder', { frequency: 'occasional' });
```

## Project Structure

```
background-effects-api/
├── src/
│   ├── core/
│   │   ├── BackgroundEngine.js          # Main orchestrator
│   │   ├── EffectRegistry.js            # Registers all effect types
│   │   └── AnimationController.js       # Handles animation loops
│   │
│   ├── effects/
│   │   ├── weather/
│   │   │   ├── precipitation/
│   │   │   │   ├── rain.js              # Light/medium/heavy rain
│   │   │   │   ├── drizzle.js           # Light mist rain
│   │   │   │   ├── snow.js              # Snowflakes
│   │   │   │   ├── flurries.js          # Light snow
│   │   │   │   ├── hail.js              # Hail stones
│   │   │   │   ├── sleet.js             # Ice pellets
│   │   │   │   └── freezing-rain.js     # Ice coating effect
│   │   │   │
│   │   │   ├── storms/
│   │   │   │   ├── thunderstorm.js      # Lightning + thunder
│   │   │   │   ├── lightning.js         # Just lightning strikes
│   │   │   │   ├── blizzard.js          # Heavy snow + wind
│   │   │   │   ├── tornado.js           # Spinning vortex effect
│   │   │   │   ├── hurricane.js         # Swirling wind + rain
│   │   │   │   └── microburst.js        # Sudden downpour
│   │   │   │
│   │   │   ├── atmospheric/
│   │   │   │   ├── fog.js               # Dense fog
│   │   │   │   ├── mist.js              # Light fog
│   │   │   │   ├── haze.js              # Hazy atmosphere
│   │   │   │   ├── smog.js              # Urban pollution
│   │   │   │   ├── ice-fog.js           # Frozen fog crystals
│   │   │   │   └── whiteout.js          # Complete visibility loss
│   │   │   │
│   │   │   ├── wind/
│   │   │   │   ├── breeze.js            # Gentle wind
│   │   │   │   ├── windy.js             # Strong wind
│   │   │   │   ├── gusty.js             # Wind bursts
│   │   │   │   ├── gale.js              # Very strong wind
│   │   │   │   ├── sandstorm.js         # Sand particles
│   │   │   │   └── dust-devil.js        # Spinning dust
│   │   │   │
│   │   │   ├── clouds/
│   │   │   │   ├── clear-sky.js         # Minimal clouds
│   │   │   │   ├── partly-cloudy.js     # Some clouds
│   │   │   │   ├── cloudy.js            # Many clouds
│   │   │   │   ├── overcast.js          # Full cloud cover
│   │   │   │   └── storm-clouds.js      # Dark dramatic clouds
│   │   │   │
│   │   │   └── special/
│   │   │       ├── diamond-dust.js      # Ice crystals in air
│   │   │       ├── ash-fall.js          # Volcanic ash
│   │   │       ├── pollen.js            # Spring pollen
│   │   │       └── aurora.js            # Northern lights
│   │   │
│   │   ├── seasonal/
│   │   │   ├── spring/
│   │   │   │   ├── cherry-blossoms.js   # Falling petals
│   │   │   │   ├── flower-petals.js     # Various flowers
│   │   │   │   ├── butterflies.js       # Flying butterflies
│   │   │   │   └── spring-rain.js       # Fresh rain
│   │   │   │
│   │   │   ├── summer/
│   │   │   │   ├── heat-waves.js        # Heat distortion
│   │   │   │   ├── fireflies.js         # Evening glows
│   │   │   │   ├── sun-rays.js          # Light beams
│   │   │   │   └── lazy-clouds.js       # Slow moving clouds
│   │   │   │
│   │   │   ├── autumn/
│   │   │   │   ├── falling-leaves.js    # Colorful leaves
│   │   │   │   ├── leaf-piles.js        # Leaf accumulation
│   │   │   │   ├── harvest-dust.js      # Golden particles
│   │   │   │   └── cool-breeze.js       # Crisp wind
│   │   │   │
│   │   │   └── winter/
│   │   │       ├── frost-formation.js   # Growing ice crystals
│   │   │       ├── icicles.js           # Dripping/forming icicles
│   │   │       ├── frozen-breath.js     # Breath vapor
│   │   │       └── ice-patterns.js      # Window frost patterns
│   │   │
│   │   ├── time-of-day/
│   │   │   ├── dawn/
│   │   │   │   ├── sunrise.js           # Sun rising
│   │   │   │   ├── morning-mist.js      # Ground fog clearing
│   │   │   │   └── birds.js             # Flying birds
│   │   │   │
│   │   │   ├── day/
│   │   │   │   ├── bright-sky.js        # Daytime sky
│   │   │   │   ├── sun-glare.js         # Sun lens flare
│   │   │   │   └── shadows.js           # Moving shadows
│   │   │   │
│   │   │   ├── dusk/
│   │   │   │   ├── sunset.js            # Sun setting
│   │   │   │   ├── golden-hour.js       # Warm lighting
│   │   │   │   └── bats.js              # Flying bats
│   │   │   │
│   │   │   └── night/
│   │   │       ├── starfield.js         # Stars twinkling
│   │   │       ├── shooting-stars.js    # Meteors
│   │   │       ├── moon-phases.js       # Moon appearance
│   │   │       ├── moonlight.js         # Moon glow
│   │   │       └── constellations.js    # Star patterns
│   │   │
│   │   ├── particles/
│   │   │   ├── nature/
│   │   │   │   ├── fireflies.js         # Glowing bugs
│   │   │   │   ├── dust-motes.js        # Floating dust
│   │   │   │   ├── seeds.js             # Dandelion seeds
│   │   │   │   └── pollen-drift.js      # Floating pollen
│   │   │   │
│   │   │   ├── magical/
│   │   │   │   ├── sparkles.js          # Glitter effect
│   │   │   │   ├── fairy-dust.js        # Magical particles
│   │   │   │   ├── energy-orbs.js       # Floating orbs
│   │   │   │   └── magic-runes.js       # Floating symbols
│   │   │   │
│   │   │   └── misc/
│   │   │       ├── bubbles.js           # Soap bubbles
│   │   │       ├── embers.js            # Fire particles
│   │   │       ├── smoke.js             # Smoke wisps
│   │   │       └── steam.js             # Steam rising
│   │   │
│   │   ├── environmental/
│   │   │   ├── water/
│   │   │   │   ├── ocean-waves.js       # Wave motion
│   │   │   │   ├── underwater.js        # Submerged view
│   │   │   │   ├── caustics.js          # Water light patterns
│   │   │   │   ├── bubbles-rising.js    # Underwater bubbles
│   │   │   │   └── ripples.js           # Water surface ripples
│   │   │   │
│   │   │   ├── forest/
│   │   │   │   ├── swaying-trees.js     # Tree movement
│   │   │   │   ├── light-rays.js        # God rays through trees
│   │   │   │   ├── forest-fog.js        # Misty forest
│   │   │   │   └── woodland-ambiance.js # Combined forest feel
│   │   │   │
│   │   │   ├── desert/
│   │   │   │   ├── heat-mirage.js       # Wavering air
│   │   │   │   ├── sand-drift.js        # Blowing sand
│   │   │   │   └── tumbleweeds.js       # Rolling plants
│   │   │   │
│   │   │   ├── mountain/
│   │   │   │   ├── snow-caps.js         # Snowy peaks
│   │   │   │   ├── avalanche.js         # Snow sliding
│   │   │   │   └── altitude-haze.js     # Thin atmosphere
│   │   │   │
│   │   │   └── cave/
│   │   │       ├── dripping-water.js    # Water drops
│   │   │       ├── stalactites.js       # Rock formations
│   │   │       └── cave-darkness.js     # Dark atmosphere
│   │   │
│   │   ├── abstract/
│   │   │   ├── gradients/
│   │   │   │   ├── color-shift.js       # Smooth transitions
│   │   │   │   ├── aurora-gradient.js   # Flowing colors
│   │   │   │   └── pulse.js             # Pulsing colors
│   │   │   │
│   │   │   ├── geometric/
│   │   │   │   ├── shapes.js            # Moving shapes
│   │   │   │   ├── polygons.js          # 3D polygons
│   │   │   │   ├── grid.js              # Grid patterns
│   │   │   │   └── fractals.js          # Fractal patterns
│   │   │   │
│   │   │   ├── digital/
│   │   │   │   ├── matrix-rain.js       # Code falling
│   │   │   │   ├── glitch.js            # Glitch effects
│   │   │   │   ├── scanlines.js         # CRT effect
│   │   │   │   └── pixel-noise.js       # Static noise
│   │   │   │
│   │   │   └── flow/
│   │   │       ├── particle-flow.js     # Flowing particles
│   │   │       ├── waves.js             # Wave patterns
│   │   │       ├── spiral.js            # Spiral motion
│   │   │       └── perlin-noise.js      # Organic flow
│   │   │
│   │   ├── tech/
│   │   │   ├── cyberpunk/
│   │   │   │   ├── neon-grid.js         # Glowing grid lines
│   │   │   │   ├── hologram.js          # Holographic effects
│   │   │   │   ├── digital-rain.js      # Falling code/glyphs
│   │   │   │   ├── circuit-board.js     # Animated circuits
│   │   │   │   └── cyber-glitch.js      # Neon glitch effects
│   │   │   │
│   │   │   ├── data/
│   │   │   │   ├── binary-stream.js     # Flowing 0s and 1s
│   │   │   │   ├── data-packets.js      # Network packets moving
│   │   │   │   ├── hex-codes.js         # Hexadecimal flowing
│   │   │   │   ├── loading-bars.js      # Progress indicators
│   │   │   │   └── data-visualization.js # Animated charts/graphs
│   │   │   │
│   │   │   ├── network/
│   │   │   │   ├── nodes-connections.js # Network topology
│   │   │   │   ├── signal-waves.js      # Radio/wifi waves
│   │   │   │   ├── server-pulses.js     # Server activity
│   │   │   │   ├── firewall.js          # Security barriers
│   │   │   │   └── packet-transfer.js   # Data moving between nodes
│   │   │   │
│   │   │   ├── futuristic/
│   │   │   │   ├── tron-grid.js         # TRON-style grid
│   │   │   │   ├── laser-beams.js       # Scanning lasers
│   │   │   │   ├── hud-elements.js      # Heads-up display
│   │   │   │   ├── portal.js            # Sci-fi portal effect
│   │   │   │   └── force-field.js       # Energy shield
│   │   │   │
│   │   │   ├── terminal/
│   │   │   │   ├── command-prompt.js    # Terminal text scrolling
│   │   │   │   ├── cursor-blink.js      # Blinking cursor
│   │   │   │   ├── compile-output.js    # Build logs scrolling
│   │   │   │   ├── error-flash.js       # Error highlighting
│   │   │   │   └── syntax-highlight.js  # Code highlighting effects
│   │   │   │
│   │   │   └── ai/
│   │   │       ├── neural-network.js    # Neural net visualization
│   │   │       ├── thinking-dots.js     # AI processing indicator
│   │   │       ├── ml-training.js       # Training visualization
│   │   │       ├── bot-activity.js      # Bot presence indicators
│   │   │       └── quantum-bits.js      # Quantum computing visual
│   │   │
│   │   └── interactive/
│   │       ├── mouse/
│   │       │   ├── cursor-trail.js      # Follows cursor
│   │       │   ├── particle-attract.js  # Attracted to cursor
│   │       │   ├── repel.js             # Repelled by cursor
│   │       │   └── orbit.js             # Orbit around cursor
│   │       │
│   │       ├── click/
│   │       │   ├── ripple.js            # Click ripples
│   │       │   ├── explosion.js         # Particle burst
│   │       │   └── shockwave.js         # Expanding ring
│   │       │
│   │       ├── scroll/
│   │       │   ├── parallax.js          # Depth layers
│   │       │   ├── reveal.js            # Scroll-triggered
│   │       │   └── transform.js         # Morph on scroll
│   │       │
│   │       └── physics/
│   │           ├── gravity.js           # Falling particles
│   │           ├── collision.js         # Bouncing
│   │           └── wind-response.js     # Wind affected
│   │
│   ├── utils/
│   │   ├── canvas.js                    # Canvas utilities
│   │   ├── color.js                     # Color manipulation
│   │   ├── math.js                      # Math helpers
│   │   └── performance.js               # Performance monitoring
│   │
│   └── presets/
│       ├── calm-morning.json            # Preset combinations
│       ├── stormy-night.json
│       ├── magical-forest.json
│       ├── cyberpunk-city.json
│       └── peaceful-autumn.json
│
├── examples/
│   ├── basic-weather.html
│   ├── seasonal-transitions.html
│   ├── interactive-demo.html
│   └── preset-showcase.html
│
├── docs/
│   ├── API.md
│   ├── creating-effects.md
│   └── performance-tips.md
│
└── package.json
```

## API Usage Example

```javascript
import BackgroundEffects from './src/core/BackgroundEngine.js';

// Initialize
const bg = new BackgroundEffects({
  container: document.getElementById('app'),
  quality: 'high' // low, medium, high
});

// Add individual effects
bg.add('rain', { intensity: 0.7, wind: 0.3 });
bg.add('fog', { density: 0.5, speed: 0.2 });
bg.add('thunderstorm', { frequency: 'occasional' });

// Or use presets
bg.loadPreset('stormy-night');

// Layer multiple effects
bg.addLayer('background', 'clouds');
bg.addLayer('midground', 'rain');
bg.addLayer('foreground', 'fog');

// Transition between effects
bg.transition('sunny', 'rainy', { duration: 3000 });

// Interactive controls
bg.setIntensity('rain', 0.9);
bg.pause('lightning');
bg.remove('snow');
bg.clear(); // Remove all effects
```

## Effect Categories

### Weather & Atmospheric
Perfect for weather apps, seasonal themes, mood setting

### Seasonal
Tie effects to specific times of year

### Time of Day
Dynamic backgrounds that match current time

### Particles
Decorative elements for ambiance

### Environmental
Immersive location-based effects

### Abstract
Modern, artistic backgrounds

### Festive
Holiday and celebration themes

### Interactive
User-responsive effects

## Configuration Options per Effect

```javascript
{
  intensity: 0-1,          // Effect strength
  speed: 0-1,              // Animation speed
  density: 0-1,            // Particle count
  color: '#hex',           // Color tint
  opacity: 0-1,            // Transparency
  blendMode: 'normal',     // Canvas blend mode
  zIndex: number,          // Layer order
  responsive: true,        // Adapt to screen size
  performance: 'auto'      // 'low', 'medium', 'high', 'auto'
}
```
