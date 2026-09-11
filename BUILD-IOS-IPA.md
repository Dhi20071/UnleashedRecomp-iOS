# UnleashedRecomp iOS / Metal GitHub Actions build

This workflow builds the current experimental iOS/Metal branch on a GitHub-hosted
macOS runner and uploads an unsigned/ad-hoc IPA as an Actions artifact.

Important:
- Do not commit Sonic Unleashed game files to a public repository.
- Put your own legally obtained `default.xex`, `default.xexp`, and `shader.ar`
  in a PRIVATE GitHub repository.
- Add two repository secrets:
    ASSET_REPO
    ASSET_REPO_TOKEN
- The workflow fetches the upstream experimental iOS branch because the ZIP
  originally supplied for this project does not contain the complete iOS/Metal
  changes.

After the workflow succeeds:
1. Open GitHub -> Actions.
2. Run "Build iOS IPA (Metal)" with "Run workflow".
3. Open the successful run.
4. Download the `Unleashed-iOS-Metal` artifact.
5. Extract it to obtain `Unleashed-iOS-Metal.ipa`.
6. Re-sign/install the IPA with your normal sideloading method.

The IPA is not App Store signed. A normal sideloading tool must re-sign it for
your Apple account/device.
