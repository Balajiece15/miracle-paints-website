# 🎯 HERO SECTION - CODE BLOCKS

Quick reference for the hero section code added to each file.

---

## 1️⃣ HTML CODE (index.html)

**Location:** Inside `<main>` tag, line 140

```html
<!-- Hero Section -->
<section id="hero" class="relative min-h-screen flex items-center justify-center overflow-hidden">
    
    <!-- Animated Background Orbs -->
    <div class="absolute inset-0 z-0">
        <div id="orb-1" class="floating-orb orb-blue"></div>
        <div id="orb-2" class="floating-orb orb-purple"></div>
        <div id="orb-3" class="floating-orb orb-pink"></div>
    </div>
    
    <!-- Hero Content -->
    <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        
        <!-- Main Headline -->
        <h1 
            class="text-5xl md:text-7xl lg:text-8xl font-bold font-poppins mb-6 leading-tight"
            data-aos="fade-up"
            data-aos-duration="1000"
        >
            <span class="block gradient-text glow-text">
                Protection First.
            </span>
            <span class="block gradient-text glow-text">
                Paint Second.
            </span>
        </h1>
        
        <!-- Subheadline -->
        <p 
            class="text-xl md:text-2xl lg:text-3xl text-gray-300 mb-12 max-w-3xl mx-auto font-light"
            data-aos="fade-up"
            data-aos-delay="200"
            data-aos-duration="1000"
        >
            Institutional coating partners for Prestige & Embassy.
        </p>
        
        <!-- CTA Buttons -->
        <div 
            class="flex flex-col sm:flex-row gap-6 justify-center items-center"
            data-aos="fade-up"
            data-aos-delay="400"
            data-aos-duration="1000"
        >
            <!-- Primary CTA - Glowing Gradient -->
            <a 
                href="#products" 
                class="group relative px-8 py-4 bg-gradient-to-r from-blue-600 to-purple-600 rounded-full font-semibold text-lg transition-all duration-300 hover:shadow-2xl hover:scale-105 overflow-hidden"
            >
                <span class="relative z-10 flex items-center">
                    Explore Solutions
                    <i class="fas fa-arrow-right ml-2 group-hover:translate-x-2 transition-transform duration-300"></i>
                </span>
                <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-purple-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300 blur-xl"></div>
            </a>
            
            <!-- Secondary CTA - Glass Outline -->
            <a 
                href="#contact" 
                class="group px-8 py-4 glassmorphism rounded-full font-semibold text-lg border-2 border-white/20 hover:border-white/40 transition-all duration-300 hover:scale-105"
            >
                <span class="flex items-center">
                    Contact Us
                    <i class="fas fa-envelope ml-2 group-hover:rotate-12 transition-transform duration-300"></i>
                </span>
            </a>
        </div>
        
        <!-- Scroll Indicator -->
        <div 
            class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce"
            data-aos="fade-up"
            data-aos-delay="800"
            data-aos-duration="1000"
        >
            <a href="#features" class="flex flex-col items-center text-gray-400 hover:text-white transition-colors duration-300">
                <span class="text-sm mb-2 font-light">Scroll to explore</span>
                <i class="fas fa-chevron-down text-2xl"></i>
            </a>
        </div>
        
    </div>
    
    <!-- Gradient Overlay for depth -->
    <div class="absolute inset-0 bg-gradient-to-b from-transparent via-transparent to-navy-900/50 pointer-events-none z-5"></div>
    
</section>
```

---

## 2️⃣ CSS CODE (styles.css)

**Location:** End of file, after line 413

```css
/* ============================================
   HERO SECTION - FLOATING ORBS
   ============================================ */

.floating-orb {
    position: absolute;
    border-radius: 50%;
    filter: blur(80px);
    opacity: 0.4;
    pointer-events: none;
    will-change: transform;
}

/* Orb 1 - Blue */
.orb-blue {
    width: 500px;
    height: 500px;
    background: radial-gradient(circle, rgba(59, 130, 246, 0.8) 0%, rgba(59, 130, 246, 0.2) 50%, transparent 100%);
    top: 10%;
    left: 10%;
}

/* Orb 2 - Purple */
.orb-purple {
    width: 600px;
    height: 600px;
    background: radial-gradient(circle, rgba(139, 92, 246, 0.8) 0%, rgba(139, 92, 246, 0.2) 50%, transparent 100%);
    top: 40%;
    right: 15%;
}

/* Orb 3 - Pink */
.orb-pink {
    width: 450px;
    height: 450px;
    background: radial-gradient(circle, rgba(236, 72, 153, 0.7) 0%, rgba(236, 72, 153, 0.2) 50%, transparent 100%);
    bottom: 20%;
    left: 30%;
}

/* Hero Section Specific Styles */
#hero {
    position: relative;
    background: linear-gradient(135deg, #0a0e27 0%, #141b2d 50%, #0f1420 100%);
}

/* Responsive Orbs for Mobile */
@media (max-width: 768px) {
    .orb-blue {
        width: 300px;
        height: 300px;
    }
    
    .orb-purple {
        width: 350px;
        height: 350px;
    }
    
    .orb-pink {
        width: 280px;
        height: 280px;
    }
}

/* Hero Headline Enhancements */
#hero h1 {
    text-shadow: 0 0 40px rgba(59, 130, 246, 0.3),
                 0 0 80px rgba(139, 92, 246, 0.2);
}

/* CTA Button Glow Animation */
@keyframes pulse-glow {
    0%, 100% {
        box-shadow: 0 0 20px rgba(59, 130, 246, 0.4),
                    0 0 40px rgba(139, 92, 246, 0.2),
                    0 10px 30px rgba(0, 0, 0, 0.3);
    }
    50% {
        box-shadow: 0 0 30px rgba(59, 130, 246, 0.6),
                    0 0 60px rgba(139, 92, 246, 0.4),
                    0 15px 40px rgba(0, 0, 0, 0.4);
    }
}

/* Apply to primary CTA */
#hero a[href="#products"] {
    animation: pulse-glow 3s ease-in-out infinite;
}
```

---

## 3️⃣ JAVASCRIPT CODE (script.js)

**Location:** After GSAP initialization, before navbar scroll effect (line 49)

```javascript
// Initialize floating orbs animation
initializeOrbAnimations();
```

**AND add this function (around line 56):**

```javascript
// ============================================
// FLOATING ORBS ANIMATION (HERO BACKGROUND)
// ============================================

function initializeOrbAnimations() {
    const orb1 = document.getElementById('orb-1');
    const orb2 = document.getElementById('orb-2');
    const orb3 = document.getElementById('orb-3');
    
    // Check if orbs exist on the page
    if (!orb1 || !orb2 || !orb3) {
        console.log('⚠ Orbs not found - skipping orb animations');
        return;
    }
    
    // Orb 1 - Blue - Slow circular motion
    gsap.to(orb1, {
        x: 100,
        y: 80,
        duration: 8,
        ease: 'sine.inOut',
        repeat: -1,
        yoyo: true
    });
    
    gsap.to(orb1, {
        scale: 1.2,
        duration: 6,
        ease: 'sine.inOut',
        repeat: -1,
        yoyo: true
    });
    
    // Orb 2 - Purple - Figure-8 motion
    gsap.to(orb2, {
        x: -120,
        y: -100,
        duration: 10,
        ease: 'sine.inOut',
        repeat: -1,
        yoyo: true
    });
    
    gsap.to(orb2, {
        scale: 0.9,
        duration: 7,
        ease: 'sine.inOut',
        repeat: -1,
        yoyo: true,
        delay: 1
    });
    
    // Orb 3 - Pink - Diagonal drift
    gsap.to(orb3, {
        x: 150,
        y: -120,
        duration: 12,
        ease: 'sine.inOut',
        repeat: -1,
        yoyo: true,
        delay: 0.5
    });
    
    gsap.to(orb3, {
        scale: 1.15,
        duration: 8,
        ease: 'sine.inOut',
        repeat: -1,
        yoyo: true,
        delay: 2
    });
    
    // Rotation for added depth
    gsap.to([orb1, orb2, orb3], {
        rotation: 360,
        duration: 20,
        ease: 'none',
        repeat: -1
    });
    
    console.log('✓ Floating Orbs Animated');
}
```

---

## ✅ INSTALLATION COMPLETE

All code has been added to the respective files. Open `index.html` in your browser to see the hero section in action!

### Expected Console Output:
```
🎨 Miracle Paints
Home Protection. Painting is Incidental.
────────────────────────────────────
Website: Ready ✓
AOS: Initialized ✓
GSAP: Initialized ✓
────────────────────────────────────
✓ AOS Initialized
✓ GSAP Initialized
✓ Floating Orbs Animated
✓ Page Loaded Successfully
✓ Miracle Paints Website Ready
```

---

## 🎯 What You'll See:

1. **Full-screen hero section** with dark gradient background
2. **3 glowing orbs** slowly floating in the background (blurred, blue/purple/pink)
3. **Headline** "Protection First. Paint Second." with gradient text and glow
4. **Subheadline** about institutional partners
5. **Two buttons:**
   - "Explore Solutions" - Glowing gradient with pulsing animation
   - "Contact Us" - Glass effect with outline
6. **Scroll indicator** at bottom with bounce animation
7. **Smooth AOS animations** as elements fade up in sequence

---

**Status:** ✅ READY TO VIEW  
**Files Modified:** 3 (index.html, styles.css, script.js)  
**Lines Added:** 267  
**New Features:** Hero Section + 3 Animated Orbs
