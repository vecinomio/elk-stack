# elk-stack

# Expected result (Test steps Gherkin style :) )
* When I access Kibana
* Then I can see a bunch of lines from source log file
* And log lines sorted by `Date` which is the first field of any line of source log file
* And I can access `Visualize` section
* And I can create a graph for any metric

# TODO
- [ ] Run Elasticsearch in docker container
- [ ] Run Logstash in docker container
- [ ] Run Kibana in docker container
- [ ] Pass to Logstash docker container sw.log file
- [ ] Configure Logstash input plugin "file" to point to sw.log
- [ ] Configure Logstash output plugin "elasticsearch" to point to Elasticsearch container
- [ ] Think about any Logstash filter plugins to be able to parse sw.log
- [ ] Metrics:
  - [ ] Memory. Search string: `resources: check_total_memory`
  - [ ] Cached hosts. Search string: `Hosts: Cached`
  - [ ] Optional:
    - [ ] Anything from `Performance Period`
