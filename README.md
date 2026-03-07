# ALICE-Animation SaaS

Anime-focused SDF direction engine API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Animation |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/render` | アニメーションレンダリング |
| `POST /api/v1/keyframe` | キーフレーム生成 |
| `GET  /api/v1/styles` | スタイル一覧 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
