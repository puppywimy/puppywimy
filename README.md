<div align="center">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 480" role="img" aria-labelledby="title description">
  <title id="title">회전하는 3D 정육면체</title>
  <desc id="description">CSS 애니메이션만으로 회전하는 정육면체입니다.</desc>
  <foreignObject width="640" height="480">
    <div xmlns="http://www.w3.org/1999/xhtml" class="stage">
      <style>
        * { box-sizing: border-box; }
        .stage {
          width: 640px; height: 480px; overflow: hidden; position: relative;
          border-radius: 32px; background: linear-gradient(135deg, #111a33, #050914);
          font-family: system-ui, sans-serif; perspective: 700px;
        }
        .cube-wrap {
          position: absolute; top: 50%; left: 50%; width: 208px; height: 208px;
          margin: -104px; transform-style: preserve-3d;
          animation: rotate-cube 7s linear infinite;
        }
        .face {
          position: absolute; inset: 0; display: grid; place-items: center;
          border: 2px solid rgba(231, 239, 255, .9); backface-visibility: visible;
          box-shadow: inset 0 0 50px rgba(255,255,255,.12);
        }
        .front  { background: #526bff; transform: translateZ(104px); }
        .back   { background: #244bc4; transform: rotateY(180deg) translateZ(104px); }
        .right  { background: #3f9cff; transform: rotateY(90deg) translateZ(104px); }
        .left   { background: #8a5cff; transform: rotateY(-90deg) translateZ(104px); }
        .top    { background: #7387ff; transform: rotateX(90deg) translateZ(104px); }
        .bottom { background: #59c9ff; transform: rotateX(-90deg) translateZ(104px); }
        .shadow {
          position: absolute; left: 50%; top: 355px; width: 240px; height: 32px;
          margin-left: -120px; border-radius: 50%; background: #000; opacity: .58;
          filter: blur(14px); animation: shadow 7s linear infinite;
        }
        .label { position: absolute; bottom: 36px; width: 100%; text-align: center; color: #9db0d8; font-size: 15px; letter-spacing: 3px; }
        @keyframes rotate-cube {
          from { transform: rotateX(-22deg) rotateY(0deg); }
          to { transform: rotateX(338deg) rotateY(360deg); }
        }
        @keyframes shadow {
          0%, 100% { transform: scaleX(.86); opacity: .45; }
          50% { transform: scaleX(1.08); opacity: .68; }
        }
      </style>
      <div class="shadow"></div>
      <div class="cube-wrap" aria-hidden="true">
        <div class="face front"></div><div class="face back"></div>
        <div class="face right"></div><div class="face left"></div>
        <div class="face top"></div><div class="face bottom"></div>
      </div>
      <div class="label">3D CUBE</div>
    </div>
  </foreignObject>
</svg>
</div>
