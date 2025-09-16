# Testing HiveBox Phase 2
   
   ## Manual Testing
   
   ### Local Python Testing
   1. Navigate to project directory
   2. Run: `python -m app.main`
   3. Expected output: "HiveBox version: 0.0.1"
   4. Verify exit code is 0
   
   ### Docker Testing
   1. Build image: `docker build -t hivebox:0.0.1 .`
   2. Run container: `docker run --rm hivebox:0.0.1`
   3. Expected output: "HiveBox version: 0.0.1"
   4. Verify container exits cleanly
   
   ## Acceptance Criteria
   - ✅ Application prints correct version (0.0.1)
   - ✅ Application exits after printing version
   - ✅ Docker image builds successfully
   - ✅ Container runs and produces expected output
   - ✅ Container exits cleanly (exit code 0)