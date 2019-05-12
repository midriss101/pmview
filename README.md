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
<ul>
  <li>Project GOC/KPI is read from (baselined) PT file.</li>
  <li>PM GOC is determined per PM Process/ output Artifact, PM GOC is calculated as follows - and written to PT file
    <ul>
      <li>25% GOC when PM starts to work on an output Artifact</li>
      <li>50% GOC when PM marks output Artifact as Ready For Review</li>
      <li>51% - 100% as each reviewer passes output Artifact - depending on number of reviewers. There is only one approver in PMView 1.1 Practitioner Edition: PM.</li>
    </ul>
  </li>
  <li>Phase GOC is aggregated from PM Process GOC, as per LCM/Process Groups Mapping</li>
</ul>

<h2 id="baselines">Baselines and Revisions</h2>
<ul>
  <li>Interim Baseline is created at project creation, comprised of an Interim Revision for each Artifact.</li>
  <li>An Interim Revision can be edited until it is approved. Once approved, it becomes an Approved Revision, and cannot be further updated. A new Interim Revision is automatically created to enable updates that will be approved in the next baseline approval.</li> 
  <li>There is no limitation to the number of Revisions (Interim or Approved) under a specific Baseline.</li>
  <li>When an Interim Baseline is approved, it cannot be edited anymore and becomes an Approved Baseline. Only Interim Baselines can be edited. All (latest) Revisions associated to the Baseline are automatically approved.</li>
  <li>When PM updates status, new revisions of concerned artifacts are created under latest Approved Baseline.</li>
</ul>

<h2 id="planning_tools">Planning Tool Integration</h2>
<ul>
  <li>PTIM integrates PMView to Planning Tools, and manages a set of Artifacts: PT Artifacts, which are:
    <ul>
      <li>WBS</li>
      <li>Schedule</li>
      <li>Activity List and Milestone List</li>
      <li>Activity Cost Estimates</li>
      <li>Activity Cost Elements</li>
    </ul>
  </li>
  <li>This applies to the following:
    <ul>
      <li>Project (Project Work)</li>
      <li>Project Management</li>
      <li>Risk Mitigation</li>
      <li>Issue Resolution</li>
      <li>Stakeholder Engagement</li>
      <li>Communication & Actions</li>
    </ul>
  </li>
</ul>
  
<h2 id="cm">Managing Project Changes</h2>
A CR can be associated to
<ul>
  <li>Requirement: Requirement Entry to be created when filling CR form</li>
  <li>WBS: If CR delivery planning results in creating new WBS entry/entries, this/these can be associated to CR</li>
</ul>

<h3>Life Cycle of a CR</h3>
<ul>
  <li>A CR is created:
    <ul>
      <li>From "Status Analysis" Panel for each PT KA, i.e. control processes</li>
      <li>New Requirement or update of existing Requirement</li>
    </ul>
  </li>
  <li>PM creates new CR Delivery Plan
    <ul>
      <li>PM selects any number of CR to include in CRDP</li>
      <li>Using PTIM, PM generates CR Artifacts (incl. Activity Estimates Sc 1)</li>
      <li>System copies project Artifacts latest baseline as CR Artifacts</li>
    </ul>
  </li>
  <li>PM refines plan as needed, and creates new Estimation Scenarios if required
    <ul>
      <li>Each CR Estimation Scenario provides delta data</li>
      <li>PM marks CRDP as Ready For Approval</li>
    </ul>
  </li>
  <li>PM marks CR as approved
    <ul>
      <li>System converts CR Artifacts as new revisions of <Project/PM/IR/SE/RM> Artifacts and approves interim baseline.</li>
    </ul>
  </li>
</ul>
