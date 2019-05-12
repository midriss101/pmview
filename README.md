# pmview
Textbook PMBOK-based project management

<a href="#project_model">Project Model</a><br>
<a href="#lifecycle">The life cycle of a project in PMView</a><br>
<a href="#goc">GOC/KPI calculation</a><br>
<a href="#baselines">Baselines and Revisions</a><br>
<a href="#planning_tools">Planning Tool Integration</a><br>
<a href="#cm">Managing Project Changes</a><br>

<h2 id="project_model">Project Model</h2>
A project is based on a Project Template, which defines
<ul>
  <li>PM Process Model</li>
  <li>Life Cycle Model</li>
  <li>How these two map to each other</li>
  <li>Artifact Templates</li>
  <li>KPI</li>
</ul>

<h2 id="lifecycle">The life cycle of a project in PMView</h2>
<ul>
  <li>A Project is created from a Project Template</li>
  <li>Preliminary LCM/PM WBS & Schedule is created during project creation</li>
  <li>Initial Baseline is setup by the system</li>
  <li>PM proceeds to progress PM deliverables from Phase View</li>
  <li>As PM works on outputs of each process, PM GOC is calculated as per below description.</li>
  <li>When the project is ready to be baselined:
    <ul>
      <li>PM approves initial Baseline, status will be measured against this baseline</li>
      <li>System creates new working Baseline, updates to Artifacts will be recorded under this baseline</li>
      <li>PM maps LCM to Project WBS</li>
      <li>LCM/PM WBS & Schedule is updated according to LCM/Project WBS mapping</li>
    </ul>
  </li>
  <li>Status against current baseline is updated into PMView as per following section.</li>
  <li>System generates Change Request candidates according to updated status.</li>
  <li>PM creates new Baselines as required. </li>
  <li>PM approves working Baseline, from now on status will be measured against this baseline</li>
  <li>PM creates new working Baseline, updates to Artifacts will be recorded under this baseline</li>
  <li>At planned end date of each phase:
    <ul>
      <li>PMView presents
          <ul>
            <li>PM GOC</li>
            <li>Project KPI</li>
          </ul>
      </li>
      <li>PM conducts Gate Review
          <ul>
            <li>System creates Gate Review objects as per LCM/PM Schedule</li>
          </ul>
      </li>
      <li>PM closes phase</li>
    </ul>
    </li>
</ul>

<h2 id="goc" >GOC/KPI calculation</h2>

<h2 id="baselines">Baselines and Revisions</h2>

<h2 id="planning_tools">Planning Tool Integration</h2>

<h2 id="cm">Managing Project Changes</h2>
