<script lang="ts">
	import type { SvelteComponent } from "svelte";
	import type { PipelineType } from "../../interfaces/Types";

	import IconAudioClassification from "../Icons/IconAudioClassification.svelte";
	import IconAudioToAudio from "../Icons/IconAudioToAudio.svelte";
	import IconAutomaticSpeechRecognition from "../Icons/IconAutomaticSpeechRecognition.svelte";
	import IconConversational from "../Icons/IconConversational.svelte";
	import IconFeatureExtraction from "../Icons/IconFeatureExtraction.svelte";
	import IconFillMask from "../Icons/IconFillMask.svelte";
	import IconImageClassification from "../Icons/IconImageClassification.svelte";
	import IconImageSegmentation from "../Icons/IconImageSegmentation.svelte";
	import IconObjectDetection from "../Icons/IconObjectDetection.svelte";
	import IconDepthEstimation from "../Icons/IconDepthEstimation.svelte";
	import IconVideoClassification from "../Icons/IconVideoClassification.svelte";
	import IconQuestionAnswering from "../Icons/IconQuestionAnswering.svelte";
	import IconSentenceSimilarity from "../Icons/IconSentenceSimilarity.svelte";
	import IconTabularClassification from "../Icons/IconTabularClassification.svelte";
	import IconTabularRegression from "../Icons/IconTabularRegression.svelte";
	import IconSummarization from "../Icons/IconSummarization.svelte";
	import IconTableQuestionAnswering from "../Icons/IconTableQuestionAnswering.svelte";
	import IconText2textGeneration from "../Icons/IconText2textGeneration.svelte";
	import IconTextClassification from "../Icons/IconTextClassification.svelte";
	import IconTextGeneration from "../Icons/IconTextGeneration.svelte";
	import IconTextToImage from "../Icons/IconTextToImage.svelte";
	import IconImageToText from "../Icons/IconImageToText.svelte";
	import IconTextToSpeech from "../Icons/IconTextToSpeech.svelte";
	import IconTokenClassification from "../Icons/IconTokenClassification.svelte";
	import IconTranslation from "../Icons/IconTranslation.svelte";
	import IconVoiceActivityDetection from "../Icons/IconVoiceActivityDetection.svelte";
	import IconZeroShotClassification from "../Icons/IconZeroShotClassification.svelte";
	import IconReinforcementLearning from "../Icons/IconReinforcementLearning.svelte";
	import IconRobotics from "../Icons/IconRobotics.svelte";
	import IconImageToImage from "../Icons/IconImageToImage.svelte";
	import IconUnconditionalImageGeneration from "../Icons/IconUnconditionalImageGeneration.svelte";
	import IconDocumentQuestionAnswering from "../Icons/IconDocumentQuestionAnswering.svelte";
	import IconGraphML from "../Icons/IconGraphML.svelte";

	export let classNames = "";
	export let pipeline = "";

	const ICON_COMPONENTS: {
		[key in PipelineType]?: typeof SvelteComponent;
	} = {
		/// Keep same order as in huggingface_hub/Types.ts
		/// for easy mapping.
		"text-classification": IconTextClassification,
		"token-classification": IconTokenClassification,
		"table-question-answering": IconTableQuestionAnswering,
		"question-answering": IconQuestionAnswering,
		"zero-shot-classification": IconZeroShotClassification,
		translation: IconTranslation,
		summarization: IconSummarization,
		conversational: IconConversational,
		"feature-extraction": IconFeatureExtraction,
		"text-generation": IconTextGeneration,
		"text2text-generation": IconText2textGeneration,
		"fill-mask": IconFillMask,
		"sentence-similarity": IconSentenceSimilarity,
		"text-to-speech": IconTextToSpeech,
		"automatic-speech-recognition": IconAutomaticSpeechRecognition,
		"audio-to-audio": IconAudioToAudio,
		"audio-classification": IconAudioClassification,
		"voice-activity-detection": IconVoiceActivityDetection,
		"depth-estimation": IconDepthEstimation,
		"image-classification": IconImageClassification,
		"object-detection": IconObjectDetection,
		"video-classification": IconVideoClassification,
		"image-segmentation": IconImageSegmentation,
		"text-to-image": IconTextToImage,
		"image-to-text": IconImageToText,
		"image-to-image": IconImageToImage,
		"unconditional-image-generation": IconUnconditionalImageGeneration,
		"reinforcement-learning": IconReinforcementLearning,
		robotics: IconRobotics,
		"graph-ml": IconGraphML,
		"tabular-classification": IconTabularClassification,
		"tabular-regression": IconTabularRegression,
		"document-question-answering": IconDocumentQuestionAnswering,
	};
</script>

<svelte:component
	this={ICON_COMPONENTS[pipeline] ?? IconFillMask}
	{classNames}
/>
