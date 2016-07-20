import kafka.producer.KeyedMessage;
import kafka.producer.ProducerConfig;
import java.util.Properties;
import kafka.javaapi.producer.Producer;
import scala.collection.Seq;

public class KafkaProducer {
  public static void main(String [] args) {
    Properties prop = new Properties();
    prop.put("metadata.broker.list", "localhost:9092,localhost:9093");
    prop.put("serializer.class","kafka.serializer.StringEncoder");
    //prop.put("partitioner.class", "example.producer.SimplePartitioner");
    ProducerConfig producerConfig = new ProducerConfig(prop);
    Producer<String,String> producer = new <String,String>Producer(producerConfig);
    String topic = "sample";
    KeyedMessage<String,String> message = new <String,String>KeyedMessage(topic, "Hello Test message");
    producer.send(message);
    producer.close();
  }
}

