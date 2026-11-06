CMS FRONTEND
yarn_action_factory


## CMS changelog summary

The private cms-frontend workflow dispatches `changelog-summary` here with an
inclusive UTC+8 date range and optional `backend,aiTutor,cmsBackend` child keys.
The main repository always participates. `include_think_and_speak` defaults to
false. CMS summaries exclude that product line, including its CMS tools, unless
the user opts in. Other CMS modules remain included. Validate and forward it as a boolean. The shared runner defaults to the
existing single-release changelog mode; summary mode reads existing Markdown
assets across all standard file prefixes, filters CMS relevance and writes all three report files only to a
private cms-frontend release. Keep `quiet` enabled; do not publish report
artifacts or text here. Existing ACCESS_TOKEN, AWS and SSM settings are reused.
Deploy api-meter's CMS summary seed and publish repo-toolkit main first.
See [the CMS guide](https://github.com/Seechange-edu/cms-frontend/blob/HEAD/docs/changelog-summary.md)
for inputs and output behavior. [中文](README.zh-CN.md).
