[tml-server-v1-plugin-3f10-ml_agenticai_restapi] Details
============================

Generated On: 2026-04-06 01:47:33 UTC

TML Solution DAG Parameters' Details: User Chosen Parametets
----------------------------

STEP 1: Get TML Core Params: `tml_system_step_1_getparams_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_1_getparams_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - solutionname
     - tml-server-v1-plugin-3f10-ml_agenticai_restapi
   * - solutiontitle
     - TML REST API Server Plugin
   * - solutiondescription
     - This is a TML server plug-in that uses REST API - allowing access from ANY application
   * - brokerhost
     - 127.0.0.1
   * - brokerport
     - 9092
   * - cloudusername
     - None
   * - ingestdatamethod
     - REST
 
STEP 2: Create Kafka Topics: `tml_system_step_2_kafka_createtopic_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_2_kafka_createtopic_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - companyname
     - Otics
   * - myname
     - Sebastian
   * - myemail
     - Sebastian.Maurice
   * - mylocation
     - Toronto
   * - replication
     - 1
   * - numpartitions
     - 1
   * - enabletls
     - 1
   * - microserviceid
     - 
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_data_topic
     - ml-data
   * - prediction_data_topic
     - prediction-data

STEP 3: `Produce to Kafka Topics <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_read_RESTAPI_step_3_kafka_producetotopic_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PRODUCETYPE
     - REST
   * - inputfile
     - --inputfile--
   * - TOPIC
     - iot-raw-data
   * - PORT
     - _39399
   * - IDENTIFIER
     - TML solution
   * - HTTPADDR
     - https://
   * - FROMHOST
     - seb,127.0.1.1
   * - TOHOST
     - 0.0.0.0
   * - CLIENTPORT
     - 9001
   * - TSS_CLIENTPORT
     - 9001
   * - TML_CLIENTPORT
     - 9002
   * - docfolder
     - --docfolderprocess--
   * - doctopic
     - --doctopic--
   * - chunks
     - --chunks--
   * - docingestinterval
     - --docingestinterval--

STEP 4: Preprocesing Data: `tml-system-step-4-kafka-preprocess-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_4_kafka_preprocess_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - preprocessconditions
     - 
   * - delay
     - 70
   * - maxrows
     - 600
   * - array
     - 0
   * - saveasarray
     - 1
   * - topicid
     - -999
   * - rawdataoutput
     - 1
   * - asynctimeout
     - 120
   * - timedelay
     - 0
   * - preprocesstypes
     - anomprob,trend,avg
   * - pathtotmlattrs
     - --pathtotmlattrs--
   * - identifier
     - IoT device performance and failures
   * - jsoncriteria
     - uid=metadata.dsn,filter:allrecords~subtopics=metadata.property_name~values=datapoint.value~identifiers=metadata.display_name~datetime=datapoint.updated_at~msgid=datapoint.id~latlong=lat:long

STEP 4a: Preprocesing Data: `tml-system-step-4a-kafka-preprocess-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_4a_kafka_preprocess_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic1--
   * - preprocess_data_topic
     - --preprocess_data_topic1--
   * - preprocessconditions
     - --preprocessconditions1--
   * - delay
     - --delay1--
   * - maxrows
     - --maxrows1--
   * - array
     - --array1--
   * - saveasarray
     - --saveasarray1--
   * - topicid
     - --topicid1--
   * - rawdataoutput
     - --rawdataoutput1--
   * - asynctimeout
     - --asynctimeout1--
   * - timedelay
     - --timedelay1--
   * - preprocesstypes
     - --preprocesstypes1--
   * - pathtotmlattrs
     - --pathtotmlattrs1--
   * - identifier
     - --identifier1--
   * - jsoncriteria
     - --jsoncriteria1--

STEP 4b: Preprocesing Data: `tml-system-step-4b-kafka-preprocess-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_4b_kafka_preprocess_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic2--
   * - preprocess_data_topic
     - --preprocess_data_topic2--
   * - preprocessconditions
     - --preprocessconditions2--
   * - delay
     - --delay2--
   * - maxrows
     - --maxrows2--
   * - array
     - --array2--
   * - saveasarray
     - --saveasarray2--
   * - topicid
     - --topicid2--
   * - rawdataoutput
     - --rawdataoutput2--
   * - asynctimeout
     - --asynctimeout2--
   * - timedelay
     - --timedelay2--
   * - preprocesstypes
     - --preprocesstypes2--
   * - pathtotmlattrs
     - --pathtotmlattrs2--
   * - identifier
     - --identifier2--
   * - jsoncriteria
     - --jsoncriteria2--

STEP 4c: Preprocesing Data: `tml-system-step-4c-kafka-preprocess-dag  <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_4c_kafka_preprocess_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic3--
   * - preprocess_data_topic
     - --preprocess_data_topic3--
   * - delay
     - --delay3--
   * - maxrows
     - --maxrows3--
   * - array
     - --array3--
   * - saveasarray
     - --saveasarray3--
   * - topicid
     - --topicid3--
   * - rawdataoutput
     - --rawdataoutput3--
   * - asynctimeout
     - --asynctimeout3--
   * - timedelay
     - --timedelay3--
   * - searchterms
     - --rtmssearchterms--
   * - rtmsstream
     - --rtmsstream--
   * - identifier
     - --identifier3--
   * - rememberpastwindows
     - --rememberpastwindows--
   * - patternwindowthreshold
     - --patternwindowthreshold--
   * - localsearchtermfolder
     - --localsearchtermfolder--
   * - localsearchtermfolderinterval
     - --localsearchtermfolderinterval--
   * - rtmsscorethreshold
     - --rtmsscorethreshold--
   * - rtmsscorethresholdtopic
     - --rtmsscorethresholdtopic--
   * - attackscorethreshold
     - --attackscorethreshold--
   * - attackscorethresholdtopic
     - --attackscorethresholdtopic--
   * - patternscorethreshold
     - --patternscorethreshold--
   * - patternscorethresholdtopic
     - --patternscorethresholdtopic--
   * - rtmsfoldername
     - --rtmsfoldername--
   * - rtmsmaxwindows
     - --rtmsmaxwindows--
   * - RTMS Output Github Link
     - `Output Data URL <--rtmsoutputurl-->`_

STEP 5: Entity Based Machine Learning : `tml-system-step-5-kafka-machine-learning-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_5_kafka_machine_learning_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_data_topic
     - ml-data
   * - modelruns
     - 10
   * - offset
     - -1
   * - islogistic
     - 1
   * - networktimeout
     - 600
   * - modelsearchtuner
     - 90
   * - processlogic
     - classification_name=failure_prob:Power_preprocessed_AnomProb=55,n
   * - dependentvariable
     - failure
   * - independentvariables
     - Power_preprocessed_AnomProb
   * - rollbackoffsets
     - 1000
   * - topicid
     - -999
   * - consumefrom
     - 
   * - fullpathtotrainingdata
     - /Viper-ml/viperlogs/iotlogistic
   * - transformtype
     - 
   * - sendcoefto
     - 
   * - coeftoprocess
     - 
   * - coefsubtopicnames
     - 
   * - ML Output Github Link
     - `Output Data URL <https:\/\/github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/mldata/iotlogistic>`_

STEP 6: Entity Based Predictions: `tml-system-step-6-kafka-predictions-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_6_kafka_predictions_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_prediction_topic
     - iot-ml-prediction-results-output
   * - streamstojoin
     - Power_preprocessed_AnomProb
   * - inputdata
     - 
   * - consumefrom
     - ml-data
   * - offset
     - -1
   * - delay
     - 70
   * - usedeploy
     - 1
   * - networktimeout
     - 600
   * - maxrows
     - 600
   * - topicid
     - -999
   * - pathtoalgos
     - /Viper-ml/viperlogs/iotlogistic

STEP 7: Real-Time Visualization: `tml-system-step-7-kafka-visualization-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_7_kafka_visualization_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - vipervizport
     - 49689
   * - topic
     - all-agents-responses,iot-preprocess,iot-ml-prediction-results-output
   * - dashboardhtml
     - iot-failure-machinelearning-agenticai.html
   * - secure
     - 1
   * - offset
     - -1
   * - append
     - 0
   * - chip
     - amd64
   * - rollbackoffset
     - 100

STEP 8: `tml_system_step_8_deploy_solution_to_docker_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_8_deploy_solution_to_docker_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Docker Container
     - maadsdocker/tml-server-v1-plugin-3f10-ml_agenticai_restapi-amd64 (https://hub.docker.com/r/maadsdocker/tml-server-v1-plugin-3f10-ml_agenticai_restapi-amd64)
   * - Docker Run Command
     - docker run -d --net=host -p 5050:5050 -p 4040:4040 -p 6060:6060 -p 9002:9002 \
          --env TSS=0 \
          --env SOLUTIONNAME=tml-server-v1-plugin-3f10-ml_agenticai_restapi \
          --env SOLUTIONDAG=solution_preprocessing_ml_agenticai_restapi_dag-tml-server-v1-plugin-3f10 \
          --env GITUSERNAME=<Enter Github Username> \
          --env GITPASSWORD='<Enter Github Password>' \          
          --env GITREPOURL=<Enter Github Repo URL> \
          --env SOLUTIONEXTERNALPORT=5050 \
          -v /var/run/docker.sock:/var/run/docker.sock:z  \
          -v /your_localmachine/foldername:/rawdata:z \
          --env CHIP=amd64 \
          --env SOLUTIONAIRFLOWPORT=4040  \
          --env SOLUTIONVIPERVIZPORT=6060 \
          --env DOCKERUSERNAME='' \
          --env CLIENTPORT=9002  \
          --env EXTERNALPORT=39399 \
          --env KAFKABROKERHOST=127.0.0.1:9092 \          
          --env KAFKACLOUDUSERNAME='<Enter API key>' \
          --env KAFKACLOUDPASSWORD='<Enter API secret>' \          
          --env SASLMECHANISM=PLAIN \          
          --env VIPERVIZPORT=49689 \
          --env MQTTUSERNAME='' \
          --env MQTTPASSWORD='' \          
          --env AIRFLOWPORT=9000  \
          --env READTHEDOCS='<Enter Readthedocs token>' \ 
          maadsdocker/tml-server-v1-plugin-3f10-ml_agenticai_restapi-amd64

STEP 9: `tml_system_step_9_privategpt_qdrant_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PrivateGPT Container
     - 
   * - PrivateGPT Run Command
     - docker run -d -p 8001:8001 --net=host --gpus all -v /var/run/docker.sock:/var/run/docker.sock:z --env PORT=8001 --env TSS=1 --env GPU=1 --env COLLECTION=tml-llm-model-v2 --env WEB_CONCURRENCY=2 --env CUDA_VISIBLE_DEVICES=0 --env TOKENIZERS_PARALLELISM=false --env temperature=0.1 --env vectorsearchtype="Manhattan" --env contextwindowsize=8192 --env vectordimension=768 
   * - Qdrant Container
     - qdrant/qdrant
   * - Qdrant Run Command
     - docker run -d -p 6333:6333 -v $(pwd)/qdrant_storage:/qdrant/storage:z qdrant/qdrant
   * - Consumefrom
     - 
   * - pgpt_data_topic
     - 
   * - offset
     - -1
   * - rollbackoffset
     - 100
   * - topicid
     - -999
   * - enabletls
     - 1
   * - partition
     - -1
   * - prompt
     - [INST] Are there any errors in the  logs? Give s detailed response including IP addresses and host machines.[/INST]
   * - context
     - This is network data from inbound and outbound packets. The data are anomaly probabilities for cyber threats from analysis of inbound and outbound packets. If inbound or outbound anomaly probabilities are less than 0.60, it is likely the risk of a cyber attack is also low. If its above 0.60, then risk is mid to high.
   * - jsonkeytogather
     - hyperprediction
   * - keyattribute
     - 
   * - keyprocesstype
     - 
   * - vectordbcollectionname
     - tml-llm-model-v2
   * - concurrency
     - 2
   * - CUDA_VISIBLE_DEVICES
     - 0
   * - pgpthost
     - http://127.0.0.1
   * - pgptport
     - 8001
   * - hyperbatch
     - 0
   * - docfolder
     - --docfolder--
   * - docfolderingestinterval
     - 900
   * - useidentifierinprompt
     - 1
   * - searchterms
     - 192.168.--identifier--,authentication failure
   * - streamall
     - 1
   * - temperature
     - 0.1
   * - vectorsearchtype
     - Manhattan
   * - llm
     - Refer to: https://tml.readthedocs.io/en/latest/genai.html
   * - embedding
     - Refer to: https://tml.readthedocs.io/en/latest/genai.html
   * - vectorsize
     - Refer to: https://tml.readthedocs.io/en/latest/genai.html
   * - contextwindowsize
     - 8192
   * - vectordimension
     - 768
   * - mitrejson
     - /rawdata/mitre.json

STEP 9b: `tml_system_step_9b_agenticai_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_9b_agenticai_dag-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - rollbackoffset
     - 5
   * - ollama-model
     - llama3.1
   * - deletevectordbcount
     - 10
   * - vectordbpath
     - /rawdata/vectordb
   * - temperature
     - 0.1
   * - topicid
     - -999
   * - enabletls
     - 1
   * - partition
     - -1
   * - vectordbcollectionname
     - tml-llm-model-v2
   * - ollamacontainername
     - 
   * - mainip
     - http://127.0.0.1
   * - mainport
     - 11434
   * - embedding
     - nomic-embed-text
   * - agenttopic
     - 
   * - agents_topic_prompt
     - 
<consumefrom - topic agent will monitor:prompt you want for the agent to answer->>consumefrom - topic2 agent will monitor<<-prompt you want for the agent to answer>

   * - teamlead_topic
     - 
   * - teamleadprompt
     - 
Enter the prompt for the Team lead agent

   * - supervisor_topic
     - 
   * - supervisorprompt
     - 
   * - agenttoolfunctions
     - 
tool_function:agent_name:system_prompt
   * - agent_team_supervisor_topic
     - 
   * - concurrency
     - 2
   * - CUDA_VISIBLE_DEVICES
     - 0
   * - contextwindow
     - 10000
   * - localmodelsfolder
     - /rawdata/ollama

STEP 10: `tml_system_step_10_documentation_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/tml-server-v1-plugin-3f10/tml_system_step_10_documentation_dag_tml-multi-agenticai-iot-3f10-tml-server-v1-plugin-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Solution Documentation URL
     - https://tml-server-v1-plugin-3f10-ml-agenticai-restapi.readthedocs.io
