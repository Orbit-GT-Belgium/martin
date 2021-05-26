# Build local
cargo build --release

# Test Local
./target/release/martin postgres://admin:WVU%26szK%267rOv0%5E%234@localhost:5432/geometries --danger-accept-invalid-certs --watch --listen-addresses=0.0.0.0:3022

# Store in Docker Hub
docker build -t orbitgtbelgium/martin .
docker push orbitgtbelgium/martin