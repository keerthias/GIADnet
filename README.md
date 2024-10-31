# GIADnet: Graph-based Intracranial Aneurysm Detection Network with Spectral Convolution

 GIADnet follows a non-Euclidean-based computing approach for aneurysm detection that uses graph-based learning to capture long-range dependencies and  learn rich representations of the cerebrovascular system. It utilizes sparsity information in the spectral domain to identify localized events in the graph structure, which can serve as strong indicators of aneurysms. 
 
# Usage
You can load the GIADnet docker image directly from the giadnet_docker.tar using the following command:
```bash
docker load < giadnet_docker.tar
```

 Then, you can run the ready-to-use icadnet_docker container with the following command:
```bash
docker run -dit --network none -v [full_path_to_input_dataset]:/input:ro -v /output giadnet_docker
```

The -v options map the input directory into the container at /input, read-only. The last -v creates an output directory.
This command outputs the Container ID,  which you can also look up with the following command:
```bash
docker ps
```
Next, you can execute the GIADnet validation script using the following command:

```bash
docker exec [CONTAINER-ID] python /GIADnet_dockerfolder/run.py
```
Finally, you can shut down the running container. This also removes the created /output folder and any other changes made to the container:

```bash
docker rm -v [CONTAINER-ID]

```

Due to memory limitations of the GitHub repository, the ready-to-use Docker container and sample dataset can be accessed via the following link: https://shorturl.at/AqMt2



