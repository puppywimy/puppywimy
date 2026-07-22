<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 480" role="img" aria-labelledby="title description">
  <defs>
    <linearGradient id="background" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#111a33"/>
      <stop offset="1" stop-color="#050914"/>
    </linearGradient>
    <filter id="blur" x="-50%" y="-100%" width="200%" height="300%">
      <feGaussianBlur stdDeviation="13"/>
    </filter>
  </defs>
  <style>
    .cube {
      transform-box: fill-box;
      transform-origin: center;
      animation: cube-spin 5s linear infinite;
    }
    .shadow {
      transform-box: fill-box;
      transform-origin: center;
      animation: shadow-pulse 5s ease-in-out infinite;
    }
    @keyframes cube-spin {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    @keyframes shadow-pulse {
      0%, 100% { transform: scaleX(.8); opacity: .34; }
      50% { transform: scaleX(1.12); opacity: .58; }
    }
  </style>

  <rect width="640" height="480" rx="32" fill="url(#background)"/>
  <ellipse class="shadow" cx="320" cy="374" rx="116" ry="18" fill="#000" filter="url(#blur)"/>
  <!-- Isometric cube: three visible faces create the 3D form. -->
  <g class="cube" stroke="#e7efff" stroke-width="2" stroke-linejoin="round">
    <polygon points="320,105 462,187 320,269 178,187" fill="#7488ff"/>
    <polygon points="178,187 320,269 320,433 178,351" fill="#795cf5"/>
    <polygon points="320,269 462,187 462,351 320,433" fill="#3f9cff"/>
    <polyline points="320,105 320,269 320,433" fill="none" stroke="#f5f8ff" stroke-opacity=".78"/>
  </g>
  <text x="320" y="450" text-anchor="middle" fill="#9db0d8" font-family="system-ui, sans-serif" font-size="15" letter-spacing="3">3D CUBE</text>
</svg>
