# CodeNarc Grails Plugin Change Log
-------------------------------------------------------------------------------
http://grails.org/plugin/codenarc

Version 1.5 (Nov 2019)
--------------------------------------
- #22: Upgrade to CodeNarc v1.5.


Version 1.4 (May 2019)
--------------------------------------
- #20: Upgrade to CodeNarc v1.4.
- #21: Use HTTPS for BuildConfig repositories


Version 1.3 (Jan 2019)
--------------------------------------
- #19: Upgrade to CodeNarc v1.3


Version 1.2.1 (Aug 2018)
--------------------------------------
- #18: Upgrade to CodeNarc v1.2.1.


Version 1.2 (Jul 2018)
--------------------------------------
- #17: Upgrade to CodeNarc v1.2.


Version 1.1 (Jan 2018)
--------------------------------------
- #16: Upgrade to CodeNarc v1.1.


Version 1.0 (Sep 2017)
--------------------------------------
- #14: Upgrade plugin to CodeNarc 1.0. That requires Groovy 2.3, which implies it is compatible only with Grails 2.4.0 or later. (So, use for Grails version >= 2.4 and < 3.x).


Version 0.27.0 (Mar 2017)
--------------------------------------
- #13: Upgrade plugin to use CodeNarc 0.27.0.


Changes in version 0.26.0 (Oct 2016)
--------------------------------------
- #11: Upgrade plugin to use CodeNarc 0.26.0.
- Upgrade project to Grails version 2.5.4.


Changes in version 0.25.2 (Apr 2016)
--------------------------------------
- #9: Upgrade plugin to use CodeNarc 0.25.2.


Changes in version 0.25.1 (Feb 2016)
--------------------------------------
- #7: Upgrade plugin to use CodeNarc 0.25.1.


Changes in version 0.24.1 (Aug 2015)
--------------------------------------
- #47: Upgrade plugin to use CodeNarc 0.24.1.
- #6: FileNotFoundException: File [null] does not exist or is not accessible.


Changes in version 0.24 (Jul 2015)
--------------------------------------
- GPCODENARC-45: Upgrade plugin to use CodeNarc 0.24.
    * Support new "sortable" and "baseline" report types.
    * Add new "excludeBaseline" configuration option for (experimental) baseline violations support. It specifies the path to a baseline violations report (report type "baseline") If set, then all violations specified within that report are excluded (filtered) from the current CodeNarc run.


Changes in version 0.23 (Feb 2015)
--------------------------------------
- GPCODENARC-44: Upgrade plugin to use CodeNarc 0.23.


Changes in version 0.22 (Sep 2014)
--------------------------------------
- Pull request #4: Upgrade to CodeNarc 0.22. (Thanks to Stefan Schöffmann)
- GPCODENARC-32: Support using custom CodeNarc rule scripts defined within the Grails project.
    Set "codenarc.useCurrentThreadContextClassLoader" system property to "true".
- GPCODENARC-43: Codenarc script should print out the list of ruleset files being used.


Changes in version 0.21 (Apr 2014)
--------------------------------------
- Upgrade to CodeNarc 0.21
- Pull request #3: Add support for 'excludes' property. (Thanks to Yuki Takei)


Changes in version 0.20 (Dec 2013)
--------------------------------------
- Upgrade to CodeNarc 0.20


Changes in version 0.19 (Jul 2013)
--------------------------------------
- Remove check for (obsolete) CodeNarc config in Config.groovy
- Upgrade to CodeNarc 0.19


Changes in version 0.18.1 (Feb 2013)
--------------------------------------
- Upgrade to CodeNarc 0.18.1


Changes in version 0.18 (Dec 2012)
--------------------------------------
- Upgrade to CodeNarc 0.18.
- GPCODENARC-33: Upgraded to Grails 2.2-RC: 'ReportsDslDelegate' has an incorrect modifier private.
- GPCODENARC-34: grails codenarc fails in case no "target" directory exists
- Migrated to new Grails Plugin Repository
- Moved source to GitHub: https://github.com/chrismair/GrailsCodeNarcPlugin.git


Changes in version 0.17 (April 2012)
--------------------------------------
- GPCODENARC-31: Upgrade to CodeNarc 0.17.
- GPCODENARC-23. Allow ruleSetFiles to be a collection/list; e.g.   codenarc.ruleSetFiles = ["rulesets/dry.xml", "rulesets/unnecessary.xml"]
- GPCODENARC-24: Create default report output file in "target" folder ("target/CodeNarcReport.html"); only used if no reports are explicitly defined.
- GPCODENARC-30. Support codenarc.properties = { GrailsPublicControllerMethod.enabled = false } in "BuildConfig.groovy"


Changes in version 0.16.1 (14 Nov 2011)
----------------------------------------
- Upgrade to CodeNarc 0.16.1
- Add extra plugin metadata to descriptor


Changes in version 0.15 (05 Aug 2011)
--------------------------------------
- Upgrade to CodeNarc 0.15
- Fix GPCODENARC-20. Create report outputFile folders if missing. See CodeNarc issue #3380494.


Changes in version 0.14 (02 Jul 2011)
--------------------------------------
- Feature: GPCODENARC-19. Upgrade to CodeNarc 0.14
- Feature: GPCODENARC-18. Move configuration to “BuildConfig.groovy”. Write out warning message if CodeNarc config still exists in “Config.groovy”.
- Fix http://jira.grails.org/browse/GPCODENARC-13. Including AbcComplexity and CyclomaticComplexity rules in ruleset makes no rules work. Include GMetrics jar as a dependency.
- Fix GPCODENARC-14. Exclude CodeNarc Plugin from war builds by default.


Changes in version 0.12 (03 Apr 2011)
--------------------------------------
- Fix #11: Allow CodeNarc rules to be applied to GSP files: http://jira.grails.org/browse/GPCODENARC-11.
  Add support in "config.groovy" for: codenarc.processViews = true
- Feature #7: Generate Multiple Reports: http://jira.grails.org/browse/GPCODENARC-7. e.g.
```
        codenarc.reports = {
            CodeNarcXmlReport('xml') {
                outputFile = 'CodeNarc-Report.xml'
                title = 'Sample Report'
            }
            CodeNarcHtmlReport('html') {
                outputFile = 'CodeNarc-Report.html'
                title = 'Sample Report'
            }
        }
```
- Fix #9: Provide error message on failure instead of throwing BuildException: http://jira.grails.org/browse/GPCODENARC-9
  Add support for systemExitOnBuildException configuration option; defaults to true.


Changes in version 0.11 (11 Mar 2011)
--------------------------------------
- Fixed dependencies so that CodeNarc jar is no longer bundled in the WAR Grails creates.


Changes in version 0.10 (6 Mar 2011)
--------------------------------------
- Upgrade to CodeNarc v0.13.


Changes in version 0.9 (20 Jan 2011)
--------------------------------------
- Upgrade to CodeNarc v0.12.
- Upgrade to Grails 1.3.4.


Changes in version 0.8.1 (25 Dec 2010)
--------------------------------------
- Fix http://jira.codehaus.org/browse/GRAILSPLUGINS-2709. “Change target named default to something else”.


Changes in version 0.8 (14 Nov 2010)
--------------------------------------
- Upgrade to CodeNarc v0.11.
- NOTE: CodeNarc v0.11 requires Groovy 1.7, so it cannot be used by projects on older versions of Grails (pre-Grails 1.3).
  For those projects, stay with CodeNarc v0.10.


Changes in version 0.7 (2 Oct 2010)
--------------------------------------
- Add support in "Config.groovy" for using a custom"codenarc.properties".
    * Support setting an optional property: e.g. codenarc.propertiesFile ="file:grails-app/conf/codenarc.properties". Prepend "file:" prefix.
- Upgrade to CodeNarc v0.10.
- Upgrade project to Grails 1.2. This does not affect the versions of Grails supported by the plugin.


Changes in version 0.6.1 (27 May 2010)
--------------------------------------
- Fix http://jira.codehaus.org/browse/GRAILSPLUGINS-2193."CodeNarc plugin doesn"t run (on Grails 1.3.1)". Explicitly set default target within"Codenarc.groovy" script.


Changes in version 0.6 (21 May 2010)
-----------------------------------
- Fix bug #1941: "Getting error trying grails codenarc using 0.4 in grails 1.2.1". http://jira.codehaus.org/browse/GRAILSPLUGINS-1941. Modify "CodeNarc.groovy" to not crash id the "Config.groovy" file is missing.
- CodeNarcRunner fixed to also println() summary in addition to LOG.info(). [Fixed in CodeNarc v0.9]
- Fix "Error executing script Codenarc: groovy.lang.MissingPropertyException: No such property: W3C_XML_SCHEMA_NS_URI for class: javax.xml.XMLConstants gant.TargetExecutionException: groovy.lang.MissingPropertyException: No such property: W3C_XML_SCHEMA_NS_URI for class". [Fixed in CodeNarc v0.9]


Changes in version 0.5 (03 Feb 2010)
------------------------------------
- Upgrade to CodeNarc 0.8.1 (bug fixes).


Changes in version 0.4 (19 Jan 2010)
------------------------------------
- Upgrade to CodeNarc 0.8. This includes XML and Text report formats (beta), a new NestedBlockDepthRule,
  enhancement of the applyToFileNames rule property to handle optional path (e.g."abc/def/MyClass.groovy").


Changes in version 0.3 (26 Aug 2009)
------------------------------------
- Upgrade to CodeNarc 0.7. This includes support for optionally prefixing ruleset file paths with "file:" to
  indicate a relative or absolute path in the filesystem rather than (the default of) being relative to the classpath.


Changes in version 0.2 (18 Jul 2009)
------------------------------------
- Add "Unused" ruleset to default rulesets.
- Upgrade to CodeNarc 0.6.
- Include "test" folders in analysis; add codenarc.processTestUnit and codenarc.processTestIntegration  properties in Config.groovy.
- Rename default report file to"CodeNarcReport.html".
- Update author and authorEmail fields in CodenarcGrailsPlugin. (Original=Burt Beckwith).
- Create automated test script for CodeNarc plugin.
- Create tests for plugin.
