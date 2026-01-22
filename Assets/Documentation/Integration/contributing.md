# Contributing to MGI Monorepo

## Pre-Export Requirements

**IMPORTANT:** Before exporting your team's package, ensure the following:

### 1. Unity Version Migration
- **All teams must upgrade to Unity 6000.3.2f1 LTS** in their own repositories
- Test and resolve all compilation errors in your team's repo first
- Ensure your build is stable and working correctly before export
- Do NOT export packages from older Unity versions

### 2. Pre-Export Checklist
- [ ] Upgraded to Unity 6.3 LTS
- [ ] All compilation errors resolved
- [ ] Build tested and working in your own repo
- [ ] All dependencies documented
- [ ] Event listeners identified (if applicable)

### 3. Package Export Process

1. **Verify Unity Version**: Confirm you're using Unity 6000.3.2f1 LTS
2. **Test Your Build**: Ensure everything works in your team's repository
3. **Resolve Errors**: Fix any compilation or runtime errors before export
4. **Export Package**:
   - Select all your team's assets from the root `Assets/` folder
   - Export as `.unitypackage` with full folder structure preserved
   - Name it: `{TeamName}_Build_v{Version}.unitypackage`
   - Include `.meta` files in export

### 4. Import Process (Integration Team)

1. **Create a new branch** for the team integration: `git checkout -b feature/integrate-{TeamName}`
2. Import package into `Assets/Teams/{TeamName}/` in Unity
3. Unity will preserve folder structure automatically, check if everything is working error free, and there are no compilation issues
4. Commit changes: `git add Assets/Teams/{TeamName}/ && git commit -m "feat: Integrate {TeamName} team package"`
5. Push branch and **create a Pull Request** for review
6. Resolve any `.meta` file conflicts (preserve GUIDs) during PR review

## Notes

- **No integration testing required before export** - teams should only ensure their own builds work
- Integration testing and cross-team validation will happen after all teams are in the monorepo
- Coordinate with integration team lead before importing if you have questions